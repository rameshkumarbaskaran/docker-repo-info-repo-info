## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:65c4a67ed5af62f50a32a2890f185bf0fa03a473a95ebd5de1a6c68c25d29795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f127770261bd54f6a6f9d62cc1ea680e78e868d20cf5bd11fe6a236202f72beb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319519648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0325acfad3ef13d4b8e1ad13d7e43ca9bad3a7a45111c70096b035b3023a4b94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:23:59 GMT
COPY dir:4f02f3c240ecc691ff41263b0454f619d51a2ba11a57fe51c0e31e7ff62a9194 in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:24:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:26:59 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 05 Jul 2023 11:26:59 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:27:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Jul 2023 11:27:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Jul 2023 11:27:16 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 11:27:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 11:27:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a077e746244337006bc6abb6a75eb4ea69a610ed50b6256900329e7736acfc`  
		Last Modified: Wed, 05 Jul 2023 11:35:40 GMT  
		Size: 192.6 MB (192580432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4229124537f12195808522a02cba488efd9a8e3d7c7e906f447f421ff887eb`  
		Last Modified: Wed, 05 Jul 2023 11:37:58 GMT  
		Size: 71.9 MB (71882902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83187c16344416f6c92cb468d0238df0e6f6e481dc15e210541b206f67e3bd30`  
		Last Modified: Wed, 05 Jul 2023 11:37:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffee3b0ad43448fcf8048723d43e73b079ae4ffd3dcaf5185949d1afc1c1e29`  
		Last Modified: Wed, 05 Jul 2023 11:37:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f4ca5574283061fd2dbd10aaa8c1c7d97d7e1bfdbab745f801b1de92b72c8184
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317094060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7f8c7032a262a1818677a592319bcdf4312076230546199feec72c0b4a0ccd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:39:26 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Wed, 05 Jul 2023 03:39:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:42:09 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 05 Jul 2023 03:42:09 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 03:42:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Jul 2023 03:42:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Jul 2023 03:42:23 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 03:42:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 03:42:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86dfcaa48ab17da652aa675b61970ff9dcd21d8083194b6bcaf57290c706ca0`  
		Last Modified: Wed, 05 Jul 2023 03:49:34 GMT  
		Size: 191.4 MB (191387642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd1bea18003bf2b0a9687cca6b941c0c3c1b82f9ebd5c2ce4b1e70ab2c944b1`  
		Last Modified: Wed, 05 Jul 2023 03:51:35 GMT  
		Size: 72.0 MB (72001423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8921a28b78df78d7ae1f129bd782ff3845a819ef74af79b3d32af94f9108e1ac`  
		Last Modified: Wed, 05 Jul 2023 03:51:29 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70a521399dd3208c1c8af73096b837f283253373265b8286cc824905f093def`  
		Last Modified: Wed, 05 Jul 2023 03:51:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
