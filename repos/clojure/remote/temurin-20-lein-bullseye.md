## `clojure:temurin-20-lein-bullseye`

```console
$ docker pull clojure@sha256:c56ba05b53fde88f592da51c8fe706608df855aaf91726187c5b94b2ad495d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b25ad7f6dcff82b24c5f0939a6162caaa0f05371cce04464b185fb9f47e09f62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227108855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1b6c5b98fd9d43c4234b84c1629a206b9104c26a921f0f673ccb4e7868d0eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:01 GMT
ADD file:144dff349a666134b5e98a9f1c6650fd9d6e4a88a6f98857f26eb84989360b91 in / 
# Thu, 07 Sep 2023 00:21:02 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 03:26:28 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:26:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:26:29 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 07 Sep 2023 03:26:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 03:26:29 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:26:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 07 Sep 2023 03:26:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 03:26:44 GMT
ENV LEIN_ROOT=1
# Thu, 07 Sep 2023 03:26:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 07 Sep 2023 03:26:47 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 03:26:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 03:26:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5dea071bb9782209397443f024a630052ab7583e365894d414f1e39cd0f65025`  
		Last Modified: Thu, 07 Sep 2023 00:25:41 GMT  
		Size: 55.1 MB (55056245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b8f8faea9607c7f73e95f0ee15b0fbfb23b2a90f8f727324186bc69f7be1ef`  
		Last Modified: Thu, 07 Sep 2023 03:34:59 GMT  
		Size: 153.8 MB (153791682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934100baaaf619770c0e3c9ab91b679a39d465cf61191e233a6e0cd632f4ee2`  
		Last Modified: Thu, 07 Sep 2023 03:34:48 GMT  
		Size: 13.9 MB (13861268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e02dc8543017480cabb1e578a6b527e39e626761bf77f7b1d11a9f9c3d06bf`  
		Last Modified: Thu, 07 Sep 2023 03:34:47 GMT  
		Size: 4.4 MB (4399260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecac44c82b005518d6a713316a1d7291c46cfd067e0b8eb5588737d80d249ec7`  
		Last Modified: Thu, 07 Sep 2023 03:34:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7ba8bb701ccb5c775f030434067bf622a4d1094dd79222f8341612ebe88cd7d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224073928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767e4f9a7a4f4460215250f1aa4fb6cf8ac6a0493ad8de7eaccd4a29d598ee7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:53:28 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:53:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 01:53:32 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 16 Aug 2023 01:53:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 01:53:32 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 01:53:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 16 Aug 2023 01:53:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 01:53:45 GMT
ENV LEIN_ROOT=1
# Wed, 16 Aug 2023 01:53:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 16 Aug 2023 01:53:47 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 01:53:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 01:53:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80577829fd2ca0f87088aee439e2af91b6b5d473c01321aca658e856bb10ee3f`  
		Last Modified: Wed, 16 Aug 2023 02:01:01 GMT  
		Size: 152.1 MB (152120028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f89476b0530c9736b4ae94a3388ab397ede8966674166604ad5787a7e09fecf`  
		Last Modified: Wed, 16 Aug 2023 02:00:52 GMT  
		Size: 13.8 MB (13849442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0d4924a8f83005ba2cc093f1237b105a0fe21322bd156ab5621d3dc1f8b30`  
		Last Modified: Wed, 16 Aug 2023 02:00:51 GMT  
		Size: 4.4 MB (4399280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c2943d1ed3c02f1ec87bd1dfea6dc33d044cefd24e9c34ce241a01d3219133`  
		Last Modified: Wed, 16 Aug 2023 02:00:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
