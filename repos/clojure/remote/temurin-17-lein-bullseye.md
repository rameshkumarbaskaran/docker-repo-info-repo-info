## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:456dc889413caad4bdc7a7d7509ae3e881e16c6a149f203d03b5f9b5297f9916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fd1faa07f5293074e72b2d53440ca344ee6e4305a6006c04380f72a6845b7f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218092860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1c2cf0adc257e7d57baec8dc46993f1531582d33ef8a2abb6722e7ddb11de4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:01 GMT
ADD file:144dff349a666134b5e98a9f1c6650fd9d6e4a88a6f98857f26eb84989360b91 in / 
# Thu, 07 Sep 2023 00:21:02 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 03:23:42 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:24:50 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 07 Sep 2023 03:24:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 03:24:50 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:25:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 07 Sep 2023 03:25:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 03:25:04 GMT
ENV LEIN_ROOT=1
# Thu, 07 Sep 2023 03:25:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 07 Sep 2023 03:25:07 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 03:25:07 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 03:25:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5dea071bb9782209397443f024a630052ab7583e365894d414f1e39cd0f65025`  
		Last Modified: Thu, 07 Sep 2023 00:25:41 GMT  
		Size: 55.1 MB (55056245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f659b2aacdd3e2363ebb3332a830f2dcd93164a10995d976ac13e700435f5`  
		Last Modified: Thu, 07 Sep 2023 03:33:07 GMT  
		Size: 144.8 MB (144775757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e41d16cf2f5918aa46cbaf4d53d40e33f73f54f560b4b90d8e054065fa66058`  
		Last Modified: Thu, 07 Sep 2023 03:33:37 GMT  
		Size: 13.9 MB (13861242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ff976243fefbb01fe052f04b1ab905aa42fac93635b2e3aaf5cce50828c63c`  
		Last Modified: Thu, 07 Sep 2023 03:33:37 GMT  
		Size: 4.4 MB (4399217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a415fee3161f889df3459c5dd32616d86233b5f70eab6e3a0382664976d9542a`  
		Last Modified: Thu, 07 Sep 2023 03:33:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e394af12c30b76661bb44a98dedae9bd2203f02c0ea806dbebb1e502e7f48ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215497423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb17bddf83265004270db42e501f7101633c5aaa2ec744b79c019844e521b0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 01:47:28 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Sat, 02 Sep 2023 01:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 01:48:58 GMT
ENV LEIN_VERSION=2.10.0
# Sat, 02 Sep 2023 01:48:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 01:48:58 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:49:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Sat, 02 Sep 2023 01:49:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 01:49:11 GMT
ENV LEIN_ROOT=1
# Sat, 02 Sep 2023 01:49:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Sat, 02 Sep 2023 01:49:13 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Sat, 02 Sep 2023 01:49:13 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Sep 2023 01:49:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c782a1c2165dbdac384abd088ebc99d9f013b55fa39e22661861b6b10083b60`  
		Last Modified: Sat, 02 Sep 2023 01:55:28 GMT  
		Size: 143.5 MB (143543490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605f4525e5838fcb4225b148e889c1cf38db785ec057c1013300789b2da9224c`  
		Last Modified: Sat, 02 Sep 2023 01:56:18 GMT  
		Size: 13.8 MB (13849473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a667b339be17f124bf8a9cc8572464fd17d40366b87891ddb35e170bc609014d`  
		Last Modified: Sat, 02 Sep 2023 01:56:18 GMT  
		Size: 4.4 MB (4399280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9a457868582fc8d126addbb551b4871f12063f0d6765a54610fecb3c2a6a8a`  
		Last Modified: Sat, 02 Sep 2023 01:56:18 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
