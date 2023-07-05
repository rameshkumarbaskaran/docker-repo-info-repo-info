## `clojure:temurin-17-tools-deps-1.11.1.1347-bullseye-slim`

```console
$ docker pull clojure@sha256:ac2e4cac2b6489d4f7e205f507aba22b15ca85645a399f108d10cf25d741fd92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1347-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8be5d34471c632a0954a75e69208650aa8edb94a8b920a71313b8ea9a43c8aea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285495432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39989f63e3d231b9398a6b7d356ae4c0ca22be3a4c1bbf3f6d583ab3f08caa34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:24:32 GMT
COPY dir:4f02f3c240ecc691ff41263b0454f619d51a2ba11a57fe51c0e31e7ff62a9194 in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:24:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:27:20 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 05 Jul 2023 11:27:20 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:27:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Jul 2023 11:27:36 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Jul 2023 11:27:36 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 11:27:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 11:27:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafbbd507c7f35e198981926b1a326f224d7e89d5a693df01bea8a92ba4e7d1b`  
		Last Modified: Wed, 05 Jul 2023 11:36:02 GMT  
		Size: 192.6 MB (192580435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062744121a547ddef9530c299df1b3fdb2a602c17473298f6c41bc964682f69c`  
		Last Modified: Wed, 05 Jul 2023 11:38:16 GMT  
		Size: 61.5 MB (61496595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048307abd6949cebb745f8321992b79d813c40352f171c93e7da7da97d0abbf`  
		Last Modified: Wed, 05 Jul 2023 11:38:09 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c02ed7f2604660c22073eb1306a19fbf106e52530e51087bcfb926d1f3bd8`  
		Last Modified: Wed, 05 Jul 2023 11:38:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1347-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17d2214f18b6981d35b5c75e66bab29cc85f765652f15026ac68da7be5531e04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283066389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cc1bf98ef7467ff292040e00f1c4243bdda3d05921c19e6a6738d3176ae66`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:39:58 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Wed, 05 Jul 2023 03:40:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:42:25 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 05 Jul 2023 03:42:25 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 03:42:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Jul 2023 03:42:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Jul 2023 03:42:39 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 03:42:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 03:42:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a44711a84ae8605b1c1f0f04cf29732536ca2ecfae7b5a7b10134f3584ec4`  
		Last Modified: Wed, 05 Jul 2023 03:49:53 GMT  
		Size: 191.4 MB (191387679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0f15f124f6b80c24788873a6c2fdfc1321a499c88ca8427255ab1fb5689198`  
		Last Modified: Wed, 05 Jul 2023 03:51:52 GMT  
		Size: 61.6 MB (61614740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bb2cc1b12359b50da0c148c4284c0ea9493a53995828e054d0b075803b28b5`  
		Last Modified: Wed, 05 Jul 2023 03:51:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b75f2b34839fb6835b459a0389150ad66f630cf12a41ca9833c0c05453ec2ef`  
		Last Modified: Wed, 05 Jul 2023 03:51:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
