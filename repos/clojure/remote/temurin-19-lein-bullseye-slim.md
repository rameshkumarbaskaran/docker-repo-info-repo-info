## `clojure:temurin-19-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:e084d30c6ed7400d9ac43f2f52b9e0f293ef41273c5abedaad35322b1a285575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:38777162b758be08603254ab2d110ce0e72e723c03a3daf5af97b811049b5d46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249644395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27edbf63086151337149c772798d9cde12de5a7331a4dc567d5446aa3f4420bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:40:49 GMT
COPY dir:49a4548ab030e4d26793e92b4d74537cf530961ce7b4083b8d383585c96415d5 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:41:51 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 05 Oct 2022 01:41:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:41:52 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:42:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Oct 2022 01:42:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:42:07 GMT
ENV LEIN_ROOT=1
# Wed, 05 Oct 2022 01:42:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Oct 2022 01:42:10 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:42:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:42:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e7de30eb4e390cffd51e73ffc9a011f0684ec59cf871eeee7182269b9d6507`  
		Last Modified: Wed, 05 Oct 2022 01:52:11 GMT  
		Size: 200.8 MB (200843776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae803b7e42259150728c6e02ae39ed2db0299c1de6fdc0a03f459906a26c42c`  
		Last Modified: Wed, 05 Oct 2022 01:52:35 GMT  
		Size: 13.0 MB (12981418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d413179e96b6116658c70187ba0e5024c3b282ffce4eb2a273c4bd51dee6d64`  
		Last Modified: Wed, 05 Oct 2022 01:52:34 GMT  
		Size: 4.4 MB (4398699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c77e676539c80c8a92fbd28ecb17f595607b77005346a466f6611f6e407db58`  
		Last Modified: Wed, 05 Oct 2022 01:52:34 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2c9dfa0e45cae1194cc973d18ffa01362afb6f670c526f2fe8e2eb27df9edcf3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246810422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c2517cd1ed60399e08fcda1f379a3b8af24170a243fb92a25404a349b34836`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:05:12 GMT
COPY dir:58f6c37df253d3555e493197f96e3f21593e31d3faf1967e0a7b9d8f0ae9e30c in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:05:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:06:29 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 05 Oct 2022 01:06:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:06:31 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:06:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Oct 2022 01:06:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:06:58 GMT
ENV LEIN_ROOT=1
# Wed, 05 Oct 2022 01:07:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Oct 2022 01:07:03 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:07:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:07:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451966db02aec3760efec5b561c0d414315fc69df240034894ad8f6005b785c0`  
		Last Modified: Wed, 05 Oct 2022 01:21:02 GMT  
		Size: 199.6 MB (199582873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fa679a95179bd22fd35a6f569bf9a96938031cba8f8c83639bc792cc6faf1f`  
		Last Modified: Wed, 05 Oct 2022 01:21:31 GMT  
		Size: 12.8 MB (12764156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249af554c9cc13b1186c52ea94ba7a1bd267dd8395678eb78dfb5aff7887b124`  
		Last Modified: Wed, 05 Oct 2022 01:21:31 GMT  
		Size: 4.4 MB (4398597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a1e5a78cfc6a851fbdbcdb45097a7f5f86c94478e6c6d6dfa6680437405319`  
		Last Modified: Wed, 05 Oct 2022 01:21:30 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
