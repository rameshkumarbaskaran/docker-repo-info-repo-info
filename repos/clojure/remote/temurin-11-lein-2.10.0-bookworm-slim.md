## `clojure:temurin-11-lein-2.10.0-bookworm-slim`

```console
$ docker pull clojure@sha256:98a62ecb9e82dcf6b9eaf9e9b95e375256a04cda782f3d4f59ff6a75e43cd7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.10.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6b31bce00c0804962a6473a16908066472bb61a409cd2c5b7880aa2089540f2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193376420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb4bb9f569850c8032e25e4ebd4a8c6d056b3b2e11208378cd387567e871280`
-	Default Command: `["lein","repl"]`

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
# Fri, 13 Oct 2023 01:32:26 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:32:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:32:26 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:32:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:32:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:32:41 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:32:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:32:43 GMT
CMD ["lein" "repl"]
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
	-	`sha256:54a78ad8a925cce1dc618a28eafb17619e2b42052b5ab459d11e600f6814ee8e`  
		Last Modified: Fri, 13 Oct 2023 01:47:05 GMT  
		Size: 15.0 MB (15001307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d232957a7f1ed4d7d78505a38debeb6e84328e608a564bcb7adbea6c74495917`  
		Last Modified: Fri, 13 Oct 2023 01:47:04 GMT  
		Size: 4.4 MB (4399286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.10.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f7e71a3abd648ca1a9e8c385d9a41a99aafb99c3740801cf5605c0c33abe3345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189973240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf2fff688439273eb95d971ba4cb2a6622a2f8ad80da8464a34ad04d65f8d40`
-	Default Command: `["lein","repl"]`

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
# Fri, 13 Oct 2023 01:03:36 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:03:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:03:36 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:03:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:03:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:03:49 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:03:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:03:52 GMT
CMD ["lein" "repl"]
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
	-	`sha256:342695ccffd455cbb1990f8d5420f48734c2ff6e7eb71b19b4beda5fd18a41ea`  
		Last Modified: Fri, 13 Oct 2023 01:15:50 GMT  
		Size: 14.8 MB (14824038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b9fdcf642500b70217cc96457c3adf9f445ea5f818ebb9d223335f434b331d`  
		Last Modified: Fri, 13 Oct 2023 01:15:49 GMT  
		Size: 4.4 MB (4399231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
