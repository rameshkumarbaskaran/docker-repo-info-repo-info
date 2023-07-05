## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:916c4da34d5011bb456e003766b72066f569a0273756b4f6500c7649ea83cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8cd53527c70110b6451d063a9e9cdcc76571500f5030ef5a4b6fc44b217b89fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325487798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8bcdddcef6b5eb62f9f0c4b619f4173a21b25abe5d99c0ec6f312289cbc058`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:18:57 GMT
COPY dir:3cd19417e6ca044e31be7ef3c49c7d24f962c0f648fd205b421373092856c87f in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:18:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:22:29 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 05 Jul 2023 11:22:29 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:22:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Jul 2023 11:22:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Jul 2023 11:22:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f32c79546e308866ce38369edf4614a73777193f0a490707182288427a0b9a`  
		Last Modified: Wed, 05 Jul 2023 11:32:34 GMT  
		Size: 198.5 MB (198549453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87849fd2df727a44b349a0ec9efbd5309753987073a75145c77c606e829c730b`  
		Last Modified: Wed, 05 Jul 2023 11:34:21 GMT  
		Size: 71.9 MB (71882429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051cd579d16340382fbf8d08a47c1d551d22d2e523c0514631adf4de4a3d9915`  
		Last Modified: Wed, 05 Jul 2023 11:34:13 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2d58cff9b20d52562aa2796a647e9719ebbd7bbe6127b0f8bd67b88b7cda7810
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (321030131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc5f2fbffeb9f507a0db982904199c7ea10bed80f71f1a09bc78d0aa504325a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:35:08 GMT
COPY dir:46f070668c95bcfc449ea3e3aa03838e4c3f9939658e6aebe91ca179e673aded in /opt/java/openjdk 
# Wed, 05 Jul 2023 03:35:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:38:18 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 05 Jul 2023 03:38:18 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 03:38:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Jul 2023 03:38:36 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Jul 2023 03:38:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c920af0a750cfe7216c4049f78b2268ce2ca834ae686e6958f0239f3f792261a`  
		Last Modified: Wed, 05 Jul 2023 03:46:39 GMT  
		Size: 195.3 MB (195324201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c1d2cc0d909f72af65de40b8c980236fb4e53b78ee5272076b55114998055e`  
		Last Modified: Wed, 05 Jul 2023 03:48:21 GMT  
		Size: 72.0 MB (72001334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba02de05ee6702e433ab941d318780c0771eeffc101169216c3dce4f27c78682`  
		Last Modified: Wed, 05 Jul 2023 03:48:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
