## `clojure:temurin-17-lein-2.10.0-bookworm`

```console
$ docker pull clojure@sha256:83118f4088170a779e062552e3713470eaf0de788895f33625e2df115b8d65b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.10.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:765ba1a032d90fa7a0aca6e44563243277ebc8b64a3a767a82eff358a7f0c7b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215790119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b4d720aa59a02a0724d453889eceb0cb82ff43ac8c33d893566a4f487e5355`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:34:01 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:34:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:35:20 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:35:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:35:20 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:35:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:35:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:35:34 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:35:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:35:37 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:35:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:35:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9297dc0c7fb70cdbd48c6c16e128659b9836a465fe2755e7b24f636c965ca5b1`  
		Last Modified: Fri, 13 Oct 2023 01:48:16 GMT  
		Size: 144.8 MB (144775739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca01f814dba9f6021a1b89c35b6fee71737aba31186c6f51d1e7a31cbafb65c`  
		Last Modified: Fri, 13 Oct 2023 01:48:54 GMT  
		Size: 17.0 MB (17032536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50cb76674d3375a6ea48f0bdda7b10312eff7f450a5f13388f9307650cf82a5`  
		Last Modified: Fri, 13 Oct 2023 01:48:53 GMT  
		Size: 4.4 MB (4399220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23b7d39e5832a08d5f3f1f40c8c566fe823a9e703c9ad7ea89bea18cf9bba03`  
		Last Modified: Fri, 13 Oct 2023 01:48:52 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.10.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c074a9bf9a636e64965024956b04a984812075617ea87c3ebf49da646a9b3046
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214410530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883c1988d70ef798d900a65865f5230cd723383fe44e3944aff001c413fa0185`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:04:48 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:04:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:06:00 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:06:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:06:00 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:06:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:06:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:06:14 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:06:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:06:16 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:06:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:06:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c0a26165e5e4720ee0810ab66a47633c5cc6f56db237748131b4b79eaf45df`  
		Last Modified: Fri, 13 Oct 2023 01:16:57 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01bd91f017cf646076c2398c69d055d3ec211b21782fc060c43c4e19588c4fa`  
		Last Modified: Fri, 13 Oct 2023 01:17:32 GMT  
		Size: 16.9 MB (16854791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb01534c01800d6928de0bd95652cb6717b6469eb7cf26ac76c629a26a65546`  
		Last Modified: Fri, 13 Oct 2023 01:17:31 GMT  
		Size: 4.4 MB (4399241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492350486b05fce68c5ce38a98434175fbaa8ce5a980333409a27cb7f576e572`  
		Last Modified: Fri, 13 Oct 2023 01:17:30 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
