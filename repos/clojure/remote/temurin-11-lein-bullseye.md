## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:4502706824c3ba50d4b7300728d990aba3f758a6fb9294fa656b816828a9b10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a772c2cf5fb3dd48348ea82bed2afd3ce2243463b3b21e78bba3637cdb42752c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271865255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfafa1f9d98ab48332e651de3d8cc011f8aac108ea8de133f286f2cd0fe3775`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:18:57 GMT
COPY dir:3cd19417e6ca044e31be7ef3c49c7d24f962c0f648fd205b421373092856c87f in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:18:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:21:02 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 05 Jul 2023 11:21:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 11:21:02 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:21:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Jul 2023 11:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 11:21:21 GMT
ENV LEIN_ROOT=1
# Wed, 05 Jul 2023 11:21:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Jul 2023 11:21:23 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f32c79546e308866ce38369edf4614a73777193f0a490707182288427a0b9a`  
		Last Modified: Wed, 05 Jul 2023 11:32:34 GMT  
		Size: 198.5 MB (198549453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c93a5f34926b62d7b1cca5817dd46df60b61490248f57523a149aa0b03a0d0`  
		Last Modified: Wed, 05 Jul 2023 11:33:33 GMT  
		Size: 13.9 MB (13861236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a2a564b942daa95abf0fc24ce5dd4d0fbfc9a31a180bde3d1a6caa58567ab3`  
		Last Modified: Wed, 05 Jul 2023 11:33:33 GMT  
		Size: 4.4 MB (4399266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3da350dc584e908d86c41b8e64c81ce97efe3d1a27be9d1dbf414a302578e121
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267276799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a598b5e6a1a93d782a9ee50dd3607540b7651c51028ffeb6f8a01fa99a9dbdc8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:35:08 GMT
COPY dir:46f070668c95bcfc449ea3e3aa03838e4c3f9939658e6aebe91ca179e673aded in /opt/java/openjdk 
# Wed, 05 Jul 2023 03:35:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:37:04 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 05 Jul 2023 03:37:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 03:37:04 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 03:37:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Jul 2023 03:37:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 03:37:18 GMT
ENV LEIN_ROOT=1
# Wed, 05 Jul 2023 03:37:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Jul 2023 03:37:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c920af0a750cfe7216c4049f78b2268ce2ca834ae686e6958f0239f3f792261a`  
		Last Modified: Wed, 05 Jul 2023 03:46:39 GMT  
		Size: 195.3 MB (195324201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b7abb7d8b9764e41d75454e507278fb5065dbd802ab612552f8446678792cd`  
		Last Modified: Wed, 05 Jul 2023 03:47:38 GMT  
		Size: 13.8 MB (13849414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b5dc31d0bcd9bf9650ecf8d26a2b4e76f42ffca77886193bc98897cb1c6503`  
		Last Modified: Wed, 05 Jul 2023 03:47:38 GMT  
		Size: 4.4 MB (4399205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
