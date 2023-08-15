## `clojure:temurin-17-tools-deps-1.11.1.1386-bullseye-slim`

```console
$ docker pull clojure@sha256:e448ab0bbdcc21df75c2b5f9bf8916b2a301223482513526620d5116ac237deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1386-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9e93a1a15a3c411078cf98e3f0057688d6f84869e6a0acf34e9b2e0363a58c2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237693598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683c988577dd0e9e45d09fd179cd1c6900b16733b71d0da29f136c7d9d5ef5b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Aug 2023 20:17:57 GMT
COPY dir:8ea3eea47bd8b9d37ce2403b2d64b2cdc0fec836a119c10ec3e4ff0bcca8bb4d in /opt/java/openjdk 
# Tue, 08 Aug 2023 22:37:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 23:24:48 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Mon, 14 Aug 2023 23:24:48 GMT
WORKDIR /tmp
# Mon, 14 Aug 2023 23:25:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 14 Aug 2023 23:25:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 14 Aug 2023 23:25:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 14 Aug 2023 23:25:05 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Aug 2023 23:25:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8050892377b9a47e9c3a9ef290967338da628f34d31341e0efc181a16a685401`  
		Last Modified: Tue, 08 Aug 2023 20:20:46 GMT  
		Size: 144.8 MB (144773775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7c071f28219f66b0d7a2958f782c8367203befe9f3020c997b8dfca8f82698`  
		Last Modified: Mon, 14 Aug 2023 23:32:51 GMT  
		Size: 61.5 MB (61501206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8261673199dcf5692c4330cc97abe8ab51aa9869a9dc3c5528a79c8c478cd5a5`  
		Last Modified: Mon, 14 Aug 2023 23:32:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70fc79944bab26ef967bcf8b1223c26921655dd067b5af7b33418bd0126e5fa`  
		Last Modified: Mon, 14 Aug 2023 23:32:44 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1386-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:47a588be76755e00caf8764089053630da68944d3d5e9c79b46c89ddec871bae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235218322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06eedca4a0b216c26e42fdbba1d7724148796f6611632ea3ee97ef1058f88bfc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:25:26 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 14:35:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Aug 2023 00:33:36 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Tue, 15 Aug 2023 00:33:37 GMT
WORKDIR /tmp
# Tue, 15 Aug 2023 00:33:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Aug 2023 00:33:51 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Aug 2023 00:33:51 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 15 Aug 2023 00:33:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Aug 2023 00:33:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc8dfc50ad1a93c8652ce31df19291350dca86cc2b7462fbd67c78d39e53aca`  
		Last Modified: Fri, 28 Jul 2023 14:27:39 GMT  
		Size: 143.5 MB (143538104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ad51948a30c5caefa663f3750eb9ae071ea34813677e6916109c9c3037fc07`  
		Last Modified: Tue, 15 Aug 2023 00:39:59 GMT  
		Size: 61.6 MB (61616369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf90bbd8bf0198b6010864593570bec76b6ac418698e041e8747bb5897095872`  
		Last Modified: Tue, 15 Aug 2023 00:39:53 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4958b7113717641761e77e4c3e6930d934177ca55095841ff20ea9aa9b456a90`  
		Last Modified: Tue, 15 Aug 2023 00:39:53 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
