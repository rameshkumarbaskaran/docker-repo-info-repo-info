## `clojure:temurin-19-lein-bullseye`

```console
$ docker pull clojure@sha256:f0879d533319270beb48cedecc492e9e823ba691e29f5555078b09de586f8c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:97ce3ef86e000c77906bc3d932f89ded91e8945364c7607c510df50e34ff12aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274555210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf290465b6830963e3aa2fc80b9060e3a7287b29ef021e549242fc830709c1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:40:10 GMT
COPY dir:49a4548ab030e4d26793e92b4d74537cf530961ce7b4083b8d383585c96415d5 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:40:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:41:27 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 05 Oct 2022 01:41:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:41:28 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:41:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Oct 2022 01:41:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:41:44 GMT
ENV LEIN_ROOT=1
# Wed, 05 Oct 2022 01:41:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Oct 2022 01:41:47 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:41:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:41:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39dc413a8bf8accdfa9d56cfc7b9aa47547fa5bfec61a15afe8626681e3df2ff`  
		Last Modified: Wed, 05 Oct 2022 01:51:46 GMT  
		Size: 200.8 MB (200843783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c7010273bddc4abb6489a0cf89fc81757edba45607259719da20218b9d44c`  
		Last Modified: Wed, 05 Oct 2022 01:52:25 GMT  
		Size: 14.3 MB (14266074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f512497d53b4f9034fc0b944aa127f2a0db60328c0e2a0453b6d04f2fb18c875`  
		Last Modified: Wed, 05 Oct 2022 01:52:24 GMT  
		Size: 4.4 MB (4398705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48336afefeb64c8c20b1dd3e3c79739d77ea74ebf2adfaefbd0ef547430bff4c`  
		Last Modified: Wed, 05 Oct 2022 01:52:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8a08bee43fcc26a96a26b45e1eecdac4aa2258b2edeccc4c05626a6becbf025a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271730716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb44e0488bd43d40edf80bdac81c7a0de2fedc5d6cf50b61a9d2f67ec2cd7d60`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:04:33 GMT
COPY dir:58f6c37df253d3555e493197f96e3f21593e31d3faf1967e0a7b9d8f0ae9e30c in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:05:56 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 05 Oct 2022 01:05:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:05:58 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:06:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 05 Oct 2022 01:06:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:06:17 GMT
ENV LEIN_ROOT=1
# Wed, 05 Oct 2022 01:06:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 05 Oct 2022 01:06:22 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:06:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:06:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf37d84f42eaa21611ea540fea88bea6b18861b24ed7b7691a2ba8a5f87f4fc`  
		Last Modified: Wed, 05 Oct 2022 01:20:34 GMT  
		Size: 199.6 MB (199582867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff8c7866385b2075462a1c1db876191b96179029914054db48959f5b121c544`  
		Last Modified: Wed, 05 Oct 2022 01:21:20 GMT  
		Size: 14.0 MB (14048213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d27e20a0a968db8adce099e0b91e59f51aeb411ed69a1a736dc0534d52e89e`  
		Last Modified: Wed, 05 Oct 2022 01:21:19 GMT  
		Size: 4.4 MB (4398610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a859c019fbf0fb78f9fab8d73e6f0a7016d720eff2cd823ef5a40351acd5340b`  
		Last Modified: Wed, 05 Oct 2022 01:21:19 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
