## `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye`

```console
$ docker pull clojure@sha256:ead1567118b4d2316ad6e89e1ff48c39c22d32f48a51915a3a10a8a341d18e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4d9239b3d9d8a8e41aef280c047d4c8e814c69064cd1a45d0c5dd14b8a9e48cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271761327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76602ae9eeafde3cd478e51f7f1c00bea8cfcc4c6bc7e0b22ce9493ea226efcb`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:37:07 GMT
COPY dir:ac445271830068829c3bd23eb1c86ee02cd9bb1649e3c49d8839a5a364b933c2 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:37:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:39:56 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 03 Oct 2023 08:39:56 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:40:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 03 Oct 2023 08:40:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 03 Oct 2023 08:40:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16734f5ea39dcb28fc0915fa8b7c5206249856dfbec50b530c6e3ef0c0848a67`  
		Last Modified: Tue, 03 Oct 2023 08:53:55 GMT  
		Size: 144.8 MB (144825964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe94a0102401ce220daf0810c6eebe600eccf0876e866839320b34dd4c1e87`  
		Last Modified: Tue, 03 Oct 2023 08:55:27 GMT  
		Size: 71.9 MB (71878031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301653b6aaf802b834b1867afc47eadd5b5c4db3095a6b94825e12f723b4c1fd`  
		Last Modified: Tue, 03 Oct 2023 08:55:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e45690a003756cc068c87472c569a3c04bb71c5bfe9ccb9aa4affe36b1a8ca40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267274027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9918fcb877ff92f0b37f63ec0e45771480c453efe562276300b6d9d3d0cb50c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:20 GMT
ADD file:46dcdcde338d2c01fed5db3fac9041736d9305145d8fc2039dd5b3714d38ede8 in / 
# Wed, 20 Sep 2023 02:44:21 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:47:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:28:30 GMT
COPY dir:17ac9e9d4b4d03adb229076835643ca11e6db9d9c122779536bfc61364556722 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:28:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:31:01 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 03 Oct 2023 08:31:01 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:31:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 03 Oct 2023 08:31:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 03 Oct 2023 08:31:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:31f5dc1f52c865588c43d8ec718f14d430e149b28f0b28232da825da7ae28f76`  
		Last Modified: Wed, 20 Sep 2023 02:47:53 GMT  
		Size: 53.7 MB (53704892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a7b8a14c04002cf8b0bce5a27e74c505c88c8c88a87b2336daf00d7b70aabe`  
		Last Modified: Tue, 03 Oct 2023 08:38:25 GMT  
		Size: 141.6 MB (141570563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a056c4acfd8744cba8abe68eeddc9ba7e56d9d791fbf8234d0fde868b714326`  
		Last Modified: Tue, 03 Oct 2023 08:39:58 GMT  
		Size: 72.0 MB (71997955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb00200c45f2512180b6abfbf291cbc01007a5c2a1c5b6ef13a8f199ca4360b8`  
		Last Modified: Tue, 03 Oct 2023 08:39:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
