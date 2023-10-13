## `clojure:latest`

```console
$ docker pull clojure@sha256:626efcc43ff07e1a7b510c2d82e055e569ed771e38e7ed936377baa5e2ba82c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:eae578f7949253314281cde36429ed1538e2b9f5eac5892c4230128fed187f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303385607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb96e76f77fb885793cee63ee6af7c19b210e3a6b91c73d17fdd6a2b0744e32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:26:37 GMT
COPY dir:beb55fdaac250289b56099cc1cfaeaa831b83d06c84fba6631b83f617b38e9e3 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:26:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:26:39 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 01:26:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:26:39 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:26:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 01:26:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:26:57 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 01:27:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 01:27:00 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:27:01 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:27:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:27:21 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:27:21 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:27:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:27:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22f852b8fd22e21a665af1df7752a2020b022c664cc83027929e2dd78557668`  
		Last Modified: Fri, 13 Oct 2023 01:43:53 GMT  
		Size: 158.6 MB (158590460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0220ca99a3dd22348714f3fad8f077b010db3eb6d62c5ca0efec9d07a7c18a3c`  
		Last Modified: Fri, 13 Oct 2023 01:43:39 GMT  
		Size: 17.0 MB (17032446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8e4c77fcc8c905f5991a90908169f5ad1c6c1d96a60bfba213764998b09443`  
		Last Modified: Fri, 13 Oct 2023 01:43:38 GMT  
		Size: 4.4 MB (4399262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12efed1a6efc0024c460113cff077cb5d3807a4233d025f5d90ff926e7bd6de5`  
		Last Modified: Fri, 13 Oct 2023 01:43:47 GMT  
		Size: 73.8 MB (73780205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be116df00197532e64fdb7e873416582578cf0a9d7b75d8efb5bd3026890c49`  
		Last Modified: Fri, 13 Oct 2023 01:43:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c865842a0f6f384800f29426512f56c32284d344a23a5a29a19c80f09964b3d7`  
		Last Modified: Fri, 13 Oct 2023 01:43:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2441baf2f8c3eb3aa4080cb688c9bede38d45e66c56ceb7228d42d6cfafbbc6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301419455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3139076746febcb7e2770bc40d79d033658ad26419c6bba57b52843fc86a5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 00:57:56 GMT
COPY dir:dad71274c7bcfed298f99738003c621c42f9777a181dc5466113abef10d5813a in /opt/java/openjdk 
# Fri, 13 Oct 2023 00:58:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 00:58:00 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 00:58:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 00:58:00 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 00:58:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 00:58:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 00:58:16 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 00:58:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 00:58:19 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 00:58:19 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 00:58:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 00:58:36 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 00:58:36 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 00:58:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 00:58:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d331f19b05c88fb3c5e4cce50330666ae97dff1cfdcc60262d3635c260452e7`  
		Last Modified: Fri, 13 Oct 2023 01:12:59 GMT  
		Size: 156.8 MB (156842642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e0996bbd6c27396ffbd62c8723162ca83cf809619444e168177c8531a1ab08`  
		Last Modified: Fri, 13 Oct 2023 01:12:48 GMT  
		Size: 16.9 MB (16854789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dae310447dc74edf3b0c4c74b5a0e52b54d691cc28dea47cb9ce03d413171e1`  
		Last Modified: Fri, 13 Oct 2023 01:12:47 GMT  
		Size: 4.4 MB (4399223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4edac04b3d67e8fa75bf71cb582eddbb03e648bab01180e35b385e54ec59ac6`  
		Last Modified: Fri, 13 Oct 2023 01:12:54 GMT  
		Size: 73.7 MB (73709208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee355c591c2dba4849badaab0bf5fa5567218e6a0366f750149301fb4248887`  
		Last Modified: Fri, 13 Oct 2023 01:12:47 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677acc6de5de1d794f74f0c6a1bed39765f851106abf6d2f950281112b55fe4b`  
		Last Modified: Fri, 13 Oct 2023 01:12:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
