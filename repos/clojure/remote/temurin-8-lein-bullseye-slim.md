## `clojure:temurin-8-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:6f3264c625648308225bb3ad3e8f41c715898de999172468869b2392ac0908bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9d9389f932b90aa7fce96b229e278899ed52780b97bb390853c3c4d4d1ccd1f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152314070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168bf66dc62874bf720bb64d654d8b36328bfd2942dcb99905f690375e834407`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:31:08 GMT
COPY dir:300027169ac55d8fb6f67a0995ca298d5de23ab51f3dc8e227f6e221abd3d2c3 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:31:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:32:17 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 05 Oct 2022 01:32:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:32:18 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:32:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Oct 2022 01:32:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:32:34 GMT
ENV LEIN_ROOT=1
# Wed, 05 Oct 2022 01:32:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Oct 2022 01:32:37 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d3b033801fe47b9b71e1e237e407fb11abe76a075f56d43fe9df4833ebe075`  
		Last Modified: Wed, 05 Oct 2022 01:46:08 GMT  
		Size: 103.5 MB (103513854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40632bc8dce5de58f100679176e8ab63ab7dcd60a4ff108ffc1829ad5c25eaa7`  
		Last Modified: Wed, 05 Oct 2022 01:46:31 GMT  
		Size: 13.0 MB (12981412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedddaafd7be7cd3e3b246cc677af9d69bd236620b28f79ae86dafcbbeaeb32`  
		Last Modified: Wed, 05 Oct 2022 01:46:30 GMT  
		Size: 4.4 MB (4398702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2ad1e4d7556b849875f82c5602dac26cc967a9de878af5e27b19f323398ce14f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149840859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194ba0a112cf660d6feb7a51eb8a27b9ebbb17d7284a6ff226280eb916c2f861`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:53:54 GMT
COPY dir:7668b70c49687fddef57006c57f288afd02ec3ccd6cde9cbc5231ec8fb9225f1 in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:53:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:55:11 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 05 Oct 2022 00:55:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 00:55:13 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 00:55:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Oct 2022 00:55:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 00:55:30 GMT
ENV LEIN_ROOT=1
# Wed, 05 Oct 2022 00:55:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Oct 2022 00:55:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911611afa665b0683fbe96bda4abb9185fe2c620cdfcc9b8a6381b9fdee36056`  
		Last Modified: Wed, 05 Oct 2022 01:13:35 GMT  
		Size: 102.6 MB (102613711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b770596793e10ba53d1518ca4297347df6e7b170bb4ca37967649aa8f25a27b9`  
		Last Modified: Wed, 05 Oct 2022 01:14:04 GMT  
		Size: 12.8 MB (12764174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7c9e3371779b5520dc163fd461c1382d6e7c860c19bf118bb73748da752949`  
		Last Modified: Wed, 05 Oct 2022 01:14:04 GMT  
		Size: 4.4 MB (4398579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
