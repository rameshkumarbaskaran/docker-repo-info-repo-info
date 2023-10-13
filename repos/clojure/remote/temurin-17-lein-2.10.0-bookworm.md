## `clojure:temurin-17-lein-2.10.0-bookworm`

```console
$ docker pull clojure@sha256:e6d1f7a0fc84107d38a263c11aad9119f64499098e105103f6f21c44481f68ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.10.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:de2ccf10e382408768e3a4482ffdc357768c7d4385918712efcbae4eb5ab37aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215789997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c1cc82ada33b5292cd778d2bcdb57b8da670bcc7b37ae6a7a080c8db28f9a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:52:06 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Fri, 13 Oct 2023 12:52:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 12:55:15 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 12:55:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 12:55:15 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 12:55:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 12:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 12:55:30 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 12:55:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 12:55:33 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 12:55:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 12:55:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f6291b22d70cff059b865d89b1554735b685fb268c97387261bac2bd8f0ee2`  
		Last Modified: Fri, 13 Oct 2023 13:09:53 GMT  
		Size: 144.8 MB (144775717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8158a3657885f88445098cee294745320e0b13ccca02fa39fff43e4ad6621c30`  
		Last Modified: Fri, 13 Oct 2023 13:11:49 GMT  
		Size: 17.0 MB (17032435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0d0ef4e63d6e663cf1ad632e8fb94781668cdc9f63e7f6eaf7c64841f1a85`  
		Last Modified: Fri, 13 Oct 2023 13:11:47 GMT  
		Size: 4.4 MB (4399220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196d5c53c41cb812a763de829939e24719c45dec49b00ddecca83eaded31de08`  
		Last Modified: Fri, 13 Oct 2023 13:11:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.10.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3346aaae00f0ccd5bd283bc40d8cb8ef5554fdecd5826a5cb3db8c541913c217
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214410452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cda30cac48f5328175c85465c0a408f563e026a0284074cf6140dbd9176ffa7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:18:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:21:23 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 10:21:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 10:21:23 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:21:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 10:21:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 10:21:36 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 10:21:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 10:21:39 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 10:21:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 10:21:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d651a3fb90463baef37e8108569d81355c0974d68da3cce0e70482f66c93d`  
		Last Modified: Fri, 13 Oct 2023 10:34:04 GMT  
		Size: 143.5 MB (143543493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced026009d240e008f4c8729c40f6863baec71b28dd450d2fab8ece597533fc`  
		Last Modified: Fri, 13 Oct 2023 10:36:47 GMT  
		Size: 16.9 MB (16854762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979aace2a27e0beee1047f17b64311f211d1d31606311bdff83917846a7194e8`  
		Last Modified: Fri, 13 Oct 2023 10:36:46 GMT  
		Size: 4.4 MB (4399220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8689ae94e278010fce3893b0d7411df08bbb4b2eb07359f6ab7695933de928`  
		Last Modified: Fri, 13 Oct 2023 10:36:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
