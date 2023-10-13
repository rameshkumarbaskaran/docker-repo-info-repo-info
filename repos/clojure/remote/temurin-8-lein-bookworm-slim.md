## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:7c56c88589c9db3107b240f5c81827d557c1642589c5c718cd514c8acc79d55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8660cb7435094833b1513c1ea8419fe80eab5827c783c569b75651e150419eb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152135494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1736c40351794dcba591c6a803b7d2b468f7e3d2456bc75989407948c7735370`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:28:08 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:28:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:29:13 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:29:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:29:13 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:29:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:29:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:29:28 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:29:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:29:30 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d25ccb95233478198757a427ee2f81fab3092542dec1b3fbcd1c703e7241ae`  
		Last Modified: Fri, 13 Oct 2023 01:44:37 GMT  
		Size: 103.6 MB (103585059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a264175066dea94501f408ec3407522933ace9712574dd4465b86d97f6a86026`  
		Last Modified: Fri, 13 Oct 2023 01:45:05 GMT  
		Size: 15.0 MB (15001277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab584d1ac13807ae8dd9e0a5a3bf8e076f424010f92c3f91acf98472ff28c00f`  
		Last Modified: Fri, 13 Oct 2023 01:45:04 GMT  
		Size: 4.4 MB (4399284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45270e171ba3c43ec8e92d9793b8f1d21559ad7729772a5c064bc54012fb6c96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151093051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ab9f163c3489add8e5dde905a7d702417fac0e66cb541b5b4fa8cd25e612bd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 00:59:52 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Fri, 13 Oct 2023 00:59:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:00:51 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:00:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:00:51 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:01:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:01:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:01:04 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:01:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:01:07 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57b690f142bf71ee0e56d780ce627f1f5444df7e8057dfc8cd7d677acefac58`  
		Last Modified: Fri, 13 Oct 2023 01:13:33 GMT  
		Size: 102.7 MB (102690507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37809987311fce371d78d725f4b2aa2051576f277e7dee8f625a3bafcab6850`  
		Last Modified: Fri, 13 Oct 2023 01:13:58 GMT  
		Size: 14.8 MB (14824031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9e48404694fc4a691ad10e073579f3fe6374005b2c462badfc85c7f41e1569`  
		Last Modified: Fri, 13 Oct 2023 01:13:57 GMT  
		Size: 4.4 MB (4399229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
