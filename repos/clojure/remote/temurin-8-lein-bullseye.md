## `clojure:temurin-8-lein-bullseye`

```console
$ docker pull clojure@sha256:9249589555ef3ea6f8a977efb05e881e3b8aab841ed6ea2c471ba9bf48601f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9f414426575458068352994e6c399b493bcfd284be40a165bc3b605f99b8bb59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176922824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa49e87d2968be6ad7d0fafe81b0dd3dc359af36bed9960b80df132216a2b576`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:51:00 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:51:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:53:59 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 02 Nov 2023 01:53:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 01:53:59 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:54:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 Nov 2023 01:54:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 01:54:15 GMT
ENV LEIN_ROOT=1
# Thu, 02 Nov 2023 01:54:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 Nov 2023 01:54:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ae3bc407ed44ee4c19e2acfaafba1a8237df1bc1f1bca7853c10d12070957d`  
		Last Modified: Thu, 02 Nov 2023 02:03:16 GMT  
		Size: 103.6 MB (103598251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd80e422946be291b8ce7eeb3ded4d4cd0fdb09326880dc22ef41b93046f371c`  
		Last Modified: Thu, 02 Nov 2023 02:04:50 GMT  
		Size: 13.9 MB (13867250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627e9dc3679bebf980de43a567542ea2a1f3778ab6b0d8ccc3bf01f9c92ab1ab`  
		Last Modified: Thu, 02 Nov 2023 02:04:50 GMT  
		Size: 4.4 MB (4399271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b54ffc703d829306a76b9c7aff3f3577f8fcbb29cd9f4de3b16d814631f795c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174664389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d951b73753acd3e4dd1faeb35abb1bb728935d19f5327f8ef149983d9111445`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:22:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 03:29:15 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 02 Nov 2023 03:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 03:31:47 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 02 Nov 2023 03:31:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 03:31:47 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 03:32:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 Nov 2023 03:32:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 03:32:02 GMT
ENV LEIN_ROOT=1
# Thu, 02 Nov 2023 03:32:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 Nov 2023 03:32:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a75e620a2c6e0a54df04b768280b9c28cb06717d56b0afd14125c17caeab1f`  
		Last Modified: Thu, 02 Nov 2023 03:38:39 GMT  
		Size: 102.7 MB (102701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dcc9031b48d5aff5f480450a64b23a6576e0ba798066aaedf4e42732f789d4`  
		Last Modified: Thu, 02 Nov 2023 03:39:58 GMT  
		Size: 13.9 MB (13855824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e910ead066e56d3fa86f1c2ad9d13766aa02d59514d2a3935253730e337737a`  
		Last Modified: Thu, 02 Nov 2023 03:39:58 GMT  
		Size: 4.4 MB (4399277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
