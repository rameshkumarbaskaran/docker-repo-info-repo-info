## `clojure:temurin-17-lein-2.10.0-bullseye`

```console
$ docker pull clojure@sha256:6400c1d568f79f3477b0be407dd0e8bb2100972fa7fcb147f2183a3d509ed91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.10.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d493b519566ac094057f4eea539889af7159acffe3d632503fb0482917ca9b9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218100681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f75132841088f24a398e8f0bded6069b515827ff056d15c347c627f5835e7d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:13 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Fri, 13 Oct 2023 12:53:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 12:56:03 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 12:56:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 12:56:03 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 12:56:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 12:56:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 12:56:19 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 12:56:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 12:56:22 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 12:56:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 12:56:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8976f0e0134f9ce5b9526072873e0aeef663c311b51134c1dcdaff7f6d97ba`  
		Last Modified: Fri, 13 Oct 2023 13:10:34 GMT  
		Size: 144.8 MB (144775767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0220bf0f91a0e6620bb1caa19cb069042d8f62e627d2201a2c761b6dca55d8d`  
		Last Modified: Fri, 13 Oct 2023 13:12:09 GMT  
		Size: 13.9 MB (13867280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772988a5ee68166a79765fad5238f5159d235d35aaa304f35729b21067acd2d8`  
		Last Modified: Fri, 13 Oct 2023 13:12:08 GMT  
		Size: 4.4 MB (4399205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3964e7505ac5d4dafac67b9a08592ebcac06bc050ac0a5911904144bf2adc867`  
		Last Modified: Fri, 13 Oct 2023 13:12:07 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.10.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0da5465adb0ea70a28fd5d7e13b7b9205cde5980b983147445f810162594ed6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215506827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fbf241f7beed353f316a2cf6268d775dbf35a27082f23f29a13515a6d81e71`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:19:41 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:22:02 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 13 Oct 2023 10:22:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 10:22:02 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:22:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 13 Oct 2023 10:22:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 10:22:15 GMT
ENV LEIN_ROOT=1
# Fri, 13 Oct 2023 10:22:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 13 Oct 2023 10:22:18 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 10:22:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 10:22:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684313f418d9fed6660cbe779ae6207c2a9b882041837ba794aa69652458352d`  
		Last Modified: Fri, 13 Oct 2023 10:34:41 GMT  
		Size: 143.5 MB (143543484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782af8da0b3a8880e2c306626527adeee738092e05b775558ce80b779ba9071a`  
		Last Modified: Fri, 13 Oct 2023 10:37:06 GMT  
		Size: 13.9 MB (13855930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8e504ac50f411484d75b9444158dee0d9bfac585a678f3927070be00ce9426`  
		Last Modified: Fri, 13 Oct 2023 10:37:05 GMT  
		Size: 4.4 MB (4399205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25c6f7bd3fa62f91e7f99eb4030797130ad88cb957cba33af321b00e8282503`  
		Last Modified: Fri, 13 Oct 2023 10:37:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
