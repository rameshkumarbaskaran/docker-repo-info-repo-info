## `clojure:temurin-8-lein-bullseye`

```console
$ docker pull clojure@sha256:c6ab76956a7cfcc7939da9ccd53a8d0230b1700f11a768100251e7eaf76afdcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4c9acf827db7c3e6bbaf6d16845c715f5fd4c8f3f9d006f2de7fe35e007d7372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177224854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13168039f4ae532d220ea07352203fd2ed92d0e7444a4327c747d9e7490f5ff8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:30:21 GMT
COPY dir:300027169ac55d8fb6f67a0995ca298d5de23ab51f3dc8e227f6e221abd3d2c3 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:31:53 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 05 Oct 2022 01:31:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:31:54 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:32:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Oct 2022 01:32:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:32:12 GMT
ENV LEIN_ROOT=1
# Wed, 05 Oct 2022 01:32:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Oct 2022 01:32:15 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff7f6c810173240005bf7ffb9ab85f81f48ebdf31fbd7f77dfae79e1c463c97`  
		Last Modified: Wed, 05 Oct 2022 01:45:49 GMT  
		Size: 103.5 MB (103513856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c215d4e140a5d6d622f8a8f1cec869f2ab3fb74b173c9a316997b46bcd3f8`  
		Last Modified: Wed, 05 Oct 2022 01:46:21 GMT  
		Size: 14.3 MB (14266084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38946c0aebe7a0a5ea422762763c9f237e8b4dc736863f97db565939df676399`  
		Last Modified: Wed, 05 Oct 2022 01:46:21 GMT  
		Size: 4.4 MB (4398666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b6bed4794d5f5ad861b3d18eb0b1237094c698ceefcf430f7586c4f1fb4e8b19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174761195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98a7bc8c1dbf0bfd9aa2dcf5fd63a4e007af51a9ebc616c06cd3b3cf9092410`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:53:17 GMT
COPY dir:7668b70c49687fddef57006c57f288afd02ec3ccd6cde9cbc5231ec8fb9225f1 in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:53:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:54:39 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 05 Oct 2022 00:54:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 00:54:41 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 00:54:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Oct 2022 00:54:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 00:54:59 GMT
ENV LEIN_ROOT=1
# Wed, 05 Oct 2022 00:55:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Oct 2022 00:55:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199e042cfdd7628b0f0e41afb373d86d7e0fb6385396b5a6fc0bec0d3533c7d6`  
		Last Modified: Wed, 05 Oct 2022 01:13:13 GMT  
		Size: 102.6 MB (102613748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b9a15cf6667fd784e490fbd0050b2361a330480eb883656e286f8fa5f866e`  
		Last Modified: Wed, 05 Oct 2022 01:13:53 GMT  
		Size: 14.0 MB (14048247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb199f897eeda1de43374d35afc36c13ff9e445498e172223bc21ac4627032c0`  
		Last Modified: Wed, 05 Oct 2022 01:13:52 GMT  
		Size: 4.4 MB (4398575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
