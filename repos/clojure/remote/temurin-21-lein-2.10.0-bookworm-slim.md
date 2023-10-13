## `clojure:temurin-21-lein-2.10.0-bookworm-slim`

```console
$ docker pull clojure@sha256:ff35a25c7059e3a8b61bbcc0556c1d010f9e093874a772c9a7a57d89e1084e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-lein-2.10.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:20b80e967eea432e8b9752812210c770845d2bf1dacc8b03d39ad5236157f894
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207141245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1f95480dc57f7e96871b778ac9566f5cff875918498c90bb93919a69641c0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:37:30 GMT
COPY dir:beb55fdaac250289b56099cc1cfaeaa831b83d06c84fba6631b83f617b38e9e3 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:37:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:37:32 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:37:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:37:32 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:37:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:37:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:37:47 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:37:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:37:50 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:37:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:37:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf5b61dfd183de50825dec7643ad1497c3b31cea76cc6371df03e0799742b5e`  
		Last Modified: Fri, 13 Oct 2023 01:50:50 GMT  
		Size: 158.6 MB (158590466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b385fbab44d2ae191a786be3aa75e733486f308e82233a4d75dfbebc46e16de`  
		Last Modified: Fri, 13 Oct 2023 01:50:38 GMT  
		Size: 15.0 MB (15001288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6169f0f2f44bf8247e9494bb50b7dfb07a591479a4742e665b7013425d5491`  
		Last Modified: Fri, 13 Oct 2023 01:50:38 GMT  
		Size: 4.4 MB (4399217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ac2aeaf5147bda02f2003031af3ee5183b7defdee2a470b53e606b448b8367`  
		Last Modified: Fri, 13 Oct 2023 01:50:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-lein-2.10.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a6a9f9aabc279d171fa0d3de02a935da74f8f25e8139e77109fcebb1cb420b37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205245603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4440beeb8cb6131707335a3fc2476d3add963a0de644a04940789c240c665d26`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:07:34 GMT
COPY dir:dad71274c7bcfed298f99738003c621c42f9777a181dc5466113abef10d5813a in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:07:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:07:38 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:07:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:07:38 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:07:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:07:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:07:51 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:07:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:07:54 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:07:54 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:07:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4870e05bb17c1acef9d3bc4bbd7fe1f561511aca70dea873243bd4aa799977`  
		Last Modified: Fri, 13 Oct 2023 01:19:07 GMT  
		Size: 156.8 MB (156842670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f06c660cffdeb694309408ba675e7633d130bb402491e55af92cc40efad159f`  
		Last Modified: Fri, 13 Oct 2023 01:18:58 GMT  
		Size: 14.8 MB (14824027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cd57cad93c33f263230152c2f65828ad41c664806b52aed1125e6b94ec0b2d`  
		Last Modified: Fri, 13 Oct 2023 01:18:57 GMT  
		Size: 4.4 MB (4399222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaf5ceb930efd25676e1ba8468ebb7a723d2a71205b950f0b47f8d8d6b8b74a`  
		Last Modified: Fri, 13 Oct 2023 01:18:57 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
