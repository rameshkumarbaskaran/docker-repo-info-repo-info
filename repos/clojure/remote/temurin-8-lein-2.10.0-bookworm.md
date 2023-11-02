## `clojure:temurin-8-lein-2.10.0-bookworm`

```console
$ docker pull clojure@sha256:f0a90fa9d5a528eddb325d5481923e8e4afb5aa095cb724ef57ef0b50538c885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-2.10.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:39c59c4579d8bf189a20bee584b4e12fe148dfa69f665ac97430c3a0e6da9335
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174609953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5de3df21cd3c723e40d083283f489e9c2ae486312f1402d3e2b417443c07b57`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:49:21 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:53:14 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 02 Nov 2023 01:53:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 01:53:14 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:53:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 Nov 2023 01:53:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 01:53:31 GMT
ENV LEIN_ROOT=1
# Thu, 02 Nov 2023 01:53:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 Nov 2023 01:53:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb39566a75265042a4da46fe895a549775ce2e985de2d6c4feb658793a1d88e`  
		Last Modified: Thu, 02 Nov 2023 02:02:40 GMT  
		Size: 103.6 MB (103598249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36f41045a931a64b47db7cb67adb2c5f1b81a6666012f379560cbe989ac6904`  
		Last Modified: Thu, 02 Nov 2023 02:04:29 GMT  
		Size: 17.0 MB (17030411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f471ccb083b7c39bc152e901d7d1eda7ffdac4569f22ff53dcdc0a127bc59b`  
		Last Modified: Thu, 02 Nov 2023 02:04:29 GMT  
		Size: 4.4 MB (4399269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-2.10.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1218480415e284415171cf92b4bd21932006d1804ddb7c026aaf46fc67e0087
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.6 MB (173565829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b6983c1b5617e3031f7a1b5f388c0712ee229699cd3ad138d18abd053ee22b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 03:28:09 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 02 Nov 2023 03:28:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 03:31:07 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 02 Nov 2023 03:31:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 03:31:07 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 03:31:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 Nov 2023 03:31:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 03:31:22 GMT
ENV LEIN_ROOT=1
# Thu, 02 Nov 2023 03:31:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 Nov 2023 03:31:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a214d30cfffddc78d15882c23dbbb68b263dad08cc11c233ef134c0c7e821fd`  
		Last Modified: Thu, 02 Nov 2023 03:38:08 GMT  
		Size: 102.7 MB (102701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29215d18bb3a8e3f0bea28769f867acb4fe918dcdc13eb24be54db3631b01221`  
		Last Modified: Thu, 02 Nov 2023 03:39:38 GMT  
		Size: 16.9 MB (16852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d626518ecb6e2263ebe6244a16c1f207adc9b8e82d4bb3a6a5da093659ae204b`  
		Last Modified: Thu, 02 Nov 2023 03:39:37 GMT  
		Size: 4.4 MB (4399238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
