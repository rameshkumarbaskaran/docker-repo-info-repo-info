## `clojure:temurin-11-tools-deps-1.11.1.1237-bullseye-slim`

```console
$ docker pull clojure@sha256:b21f751089dfe30a4b657e5a4c74a513adf4a5150cd3f29f40016e44019d995d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1237-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:869ccedebc7a607e99c1acc4923361f47c6eb46d2380fe0345ec2213f1741dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291372198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba52f52a5c96dc902167fad46b0b0f959baa690aa0741cf8381dd32551185654`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 08:55:42 GMT
COPY dir:00b91555b346efd0ed206d19de82e3af67e3591603a223e1eef0aee2c231a058 in /opt/java/openjdk 
# Thu, 02 Mar 2023 08:55:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Mar 2023 19:24:00 GMT
ENV CLOJURE_VERSION=1.11.1.1237
# Fri, 03 Mar 2023 19:24:00 GMT
WORKDIR /tmp
# Fri, 03 Mar 2023 19:24:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1cadeebb4ac96c7655f04c60369c6ea69968cc168b44e607df32aac739700751 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 03 Mar 2023 19:24:19 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 03 Mar 2023 19:24:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe464df9e08939be8903d77d5ed79aa7c6bab63ba7dd463f4b456b4fcdb5306`  
		Last Modified: Thu, 02 Mar 2023 09:12:53 GMT  
		Size: 198.5 MB (198475456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec3c2417b645e7f93dda04ce1fb199528250f317673da775a03ee68ed7a031e`  
		Last Modified: Fri, 03 Mar 2023 19:34:46 GMT  
		Size: 61.5 MB (61484722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1cc48a00b57473e4c2a92ebc7f41a26e9451768b414bec3c55b2483d46f759`  
		Last Modified: Fri, 03 Mar 2023 19:34:39 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1237-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be8f93c0c64e526873cda6d910d2774b501bfd7249a5932916022156e02eb8ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286901579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a9fb9e47671fbf30e84f3c39f28eb9033a223cc6093b686e5f1506998e7b50`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:02:38 GMT
COPY dir:10bda54a6f055ef6cbbc2c7efdd1ef99bb798b3ae26972613c5ee4e57e620aeb in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:02:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Mar 2023 19:44:18 GMT
ENV CLOJURE_VERSION=1.11.1.1237
# Fri, 03 Mar 2023 19:44:18 GMT
WORKDIR /tmp
# Fri, 03 Mar 2023 19:44:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1cadeebb4ac96c7655f04c60369c6ea69968cc168b44e607df32aac739700751 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 03 Mar 2023 19:44:32 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 03 Mar 2023 19:44:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594d0c25b8198dd3c5842d1aeb5b5630309d3dc5160dd9849d5f1ba6b3b6b55`  
		Last Modified: Thu, 02 Mar 2023 07:17:16 GMT  
		Size: 195.2 MB (195240256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70594c2d24f7cbedf06962160bc1e9a43155e8a03dd0502b3868ee80d14a941f`  
		Last Modified: Fri, 03 Mar 2023 19:52:33 GMT  
		Size: 61.6 MB (61597893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f91bb2a256adac25d3404190823e3d97acaa45defcf3c3d65325d3ec53eaab`  
		Last Modified: Fri, 03 Mar 2023 19:52:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
