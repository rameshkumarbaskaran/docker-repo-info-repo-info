## `clojure:temurin-17-lein-2.9.10-bullseye-slim`

```console
$ docker pull clojure@sha256:2c9fbb178d83006d7116bb3e8ed381477072950d64d0fd804923d19c2e6afd5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.9.10-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:257ec85a54acf0039eda81a4a336edd2e4467a81edd11c9e6b1cf02347a7e056
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240938042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381eaf4842d76fda43d62fef7b5e7c75e6f41a37d5bbcc7c7ee7e58c0d12106f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:37:41 GMT
COPY dir:4a40d0ddbd507a7d3b3a97117be800fbf93534cac954d63629e4fb22f3cd41ad in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:37:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:38:44 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 05 Oct 2022 01:38:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:38:44 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:39:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Oct 2022 01:39:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:39:00 GMT
ENV LEIN_ROOT=1
# Wed, 05 Oct 2022 01:39:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Oct 2022 01:39:03 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:39:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:39:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886809c89616aad77af0691ec37718e30fdcda3a35959fe64d1b37b7e2cfda5`  
		Last Modified: Wed, 05 Oct 2022 01:50:00 GMT  
		Size: 192.1 MB (192137460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6235ccd494d8a8c00e6265512da993097fba845e5d87760d80c2d4a9f611ca55`  
		Last Modified: Wed, 05 Oct 2022 01:50:31 GMT  
		Size: 13.0 MB (12981403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab99beb25968da958c092faaa0dffe3cd2330d0ac76544c75db061a6b07946ad`  
		Last Modified: Wed, 05 Oct 2022 01:50:31 GMT  
		Size: 4.4 MB (4398677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce546e4f13499d91576a92c612c5d1cc47b5733f9e622d56539b041611724710`  
		Last Modified: Wed, 05 Oct 2022 01:50:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.9.10-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8440431ff7f6f5b5b069d089905e09f00dd4a1307d1b3f7cb9deecce5e8db2ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 MB (238131883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79813139f67dc56b8711ac70b4fde68f7c1e49db8c1dc7272f5942ac52aae5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:01:21 GMT
COPY dir:e8b09aac8a69a5f07df362ceeac55cf5f3321b4ba40e9b02e12250e34b34e83e in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:01:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:02:40 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 05 Oct 2022 01:02:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:02:42 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:02:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Oct 2022 01:02:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:02:58 GMT
ENV LEIN_ROOT=1
# Wed, 05 Oct 2022 01:03:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Oct 2022 01:03:03 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:03:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:03:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a6c1d832d4d9011c73ee876bbbbdc9b3b0a7d057d4ff04d3b4078597e6a527`  
		Last Modified: Wed, 05 Oct 2022 01:18:30 GMT  
		Size: 190.9 MB (190904314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2b6ef2eda2b1c8396e391e8a2bf45be6edfd6f95fb3a3b8873fc3e49c8ab51`  
		Last Modified: Wed, 05 Oct 2022 01:19:03 GMT  
		Size: 12.8 MB (12764168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3654cc232198a3f26504cbf941f716f88a5d03f69b4dc09eea3364c97e73e`  
		Last Modified: Wed, 05 Oct 2022 01:19:02 GMT  
		Size: 4.4 MB (4398605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadfebb1fb5e58a73e65e0cf5f7a5d7a7d3cd43a56f401a6063b450e63eb54f2`  
		Last Modified: Wed, 05 Oct 2022 01:19:01 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
