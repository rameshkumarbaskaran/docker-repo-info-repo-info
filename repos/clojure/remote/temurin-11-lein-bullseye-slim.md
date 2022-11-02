## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:5c33bda1ab9d073a2090ae4349cc6ffb4b52db66944be182f687339ecd334db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3a59f77627bb4ea7e16ac19eda7de6290d9b9d8fccfb37c069d8783570eaa54e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246926512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71bb6cfe63475e32ef43eba33055afd0cd5acba4012bd8f904ac967e0edbf9e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:11:14 GMT
COPY dir:24028fba84faa85b57bc32be14abf8fad6a4bd4db557cb5499b6d5cf38d97646 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:12:47 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 02 Nov 2022 20:12:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:12:47 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:13:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 02 Nov 2022 20:13:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:13:03 GMT
ENV LEIN_ROOT=1
# Wed, 02 Nov 2022 20:13:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 02 Nov 2022 20:13:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9424e0e92a9d7ac25f2f902e3550e25f0379d53b383d802d0c0a9174fddd9e5d`  
		Last Modified: Wed, 02 Nov 2022 20:24:52 GMT  
		Size: 198.1 MB (198124751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968982dcdd7993c9e26cba117a3826c80988f69881cbf8132f9ae507a997a1e0`  
		Last Modified: Wed, 02 Nov 2022 20:25:35 GMT  
		Size: 13.0 MB (12983047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3278c3a8f0f0cdee801553a77fefe92af0e12f281396ccc21b99a6ec6881770c`  
		Last Modified: Wed, 02 Nov 2022 20:25:34 GMT  
		Size: 4.4 MB (4398676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1bcd4ea31f6ebec6587b3a396ef0593a0d776d472b5dd846ab7e8d2e87856a57
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242300563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6a38f531e7f4e00d5cfdcfab2e8f6aa9ae4d87a83adb8120722653e471e0be`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:47:12 GMT
COPY dir:e48336735658172388295f760b71f5f10a9b7d3f960c6e4546718a38dd6452e7 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:47:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:48:34 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 02 Nov 2022 20:48:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:48:34 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:48:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 02 Nov 2022 20:48:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:48:47 GMT
ENV LEIN_ROOT=1
# Wed, 02 Nov 2022 20:48:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 02 Nov 2022 20:48:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc966be4bd15170671412b817450394760b037c8e5e3587768bfc3bbd123d53`  
		Last Modified: Wed, 02 Nov 2022 20:58:36 GMT  
		Size: 194.9 MB (194867681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a623a82454545d4dfbafb6d4ef7cb2117452c888a107e2316cc65b2da0ffc365`  
		Last Modified: Wed, 02 Nov 2022 20:59:15 GMT  
		Size: 13.0 MB (12970303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818131bfc6b91e6f616f2dacffd253b6be9b3666ad500a1ceac96ccd2696df7e`  
		Last Modified: Wed, 02 Nov 2022 20:59:15 GMT  
		Size: 4.4 MB (4398669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
