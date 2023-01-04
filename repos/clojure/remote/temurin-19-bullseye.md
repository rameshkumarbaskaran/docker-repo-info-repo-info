## `clojure:temurin-19-bullseye`

```console
$ docker pull clojure@sha256:5770c7667b995c074be016dac120e95a1075a54c8f26d7cf1ff49a15c59f71bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4211055d7b99544e508a54ae9361991f03aa00e63626a9db49ac421df7835db4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (327987880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e115e57853415c5fbe4bab65738104d960de476549eca867575fc6a9a83cf2e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:21 GMT
ADD file:c13b430c8699df107ffd9ea5230b92238bc037a8e1cbbe35d6ab664941d575da in / 
# Wed, 21 Dec 2022 01:20:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:50:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:59:28 GMT
COPY dir:fef581854733ec7202f8c807463b9e1952aeb6c7a002719c7e54987e50ea4dcb in /opt/java/openjdk 
# Wed, 21 Dec 2022 01:59:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:01:36 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 21 Dec 2022 02:01:36 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 19:27:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 04 Jan 2023 19:27:13 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 19:27:13 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 04 Jan 2023 19:27:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Jan 2023 19:27:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:32de3c850997ce03b6ff4ae8fb00b34b9d7d7f9a35bfcdb8538e22cc7b77c29d`  
		Last Modified: Wed, 21 Dec 2022 01:24:10 GMT  
		Size: 55.0 MB (55025166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d80e226f52e65f91550fee64cdd6a467c4da00bac7bed86c44aa550b443f1d`  
		Last Modified: Wed, 21 Dec 2022 02:10:56 GMT  
		Size: 201.1 MB (201103393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c755c74846d32d2bf3e456842095823c0183d51c8704373642abc5b031ef5`  
		Last Modified: Wed, 04 Jan 2023 19:35:16 GMT  
		Size: 71.9 MB (71858300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91924f9fb36b011c858f98dcd816559344edd5c662f46691c902562f119ed89`  
		Last Modified: Wed, 04 Jan 2023 19:35:08 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6015cdbe0d2b67b7f118bdd37207e3520de0eefa70ca83a31bfd4bc93fb0fb6`  
		Last Modified: Wed, 04 Jan 2023 19:35:08 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61e9a9c5be186ab0042ddd3bd6c82348d77cfd681bfd16368ce7cf18093a7c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795ee7b681d76509d5b77d376c95bc3824cf67f752e3adea5eba4f2ecb9bafa6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:40 GMT
ADD file:5bbdc914ec8ed60ac85293e88ee1aafc3f0290762e320fc86dc9d79fa201834e in / 
# Wed, 21 Dec 2022 01:39:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:18:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 02:25:44 GMT
COPY dir:4138443eebfda1a2a245638d5bb568645bd34d79b66d39a3be31b5ac6b823d6d in /opt/java/openjdk 
# Wed, 21 Dec 2022 02:25:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 02:27:36 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 21 Dec 2022 02:27:36 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 18:45:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 04 Jan 2023 18:45:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 18:45:53 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 04 Jan 2023 18:45:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Jan 2023 18:45:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3e6129b48b69d14c5e7a5605e2b94003fb71aac82eac46b8689f5b8007af2c5`  
		Last Modified: Wed, 21 Dec 2022 01:42:49 GMT  
		Size: 53.7 MB (53681797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5504f1730ed4e1dc3a15ab910d7a54c44be3b7eaa38521d40d2d6396a25c2b74`  
		Last Modified: Wed, 21 Dec 2022 02:35:43 GMT  
		Size: 199.9 MB (199864404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adac4052fd16b16a256b3b14908fdef6e9695e0f7be712aa39774fecbd260b2c`  
		Last Modified: Wed, 04 Jan 2023 18:52:41 GMT  
		Size: 72.0 MB (71979433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b767d55b5bf9c64f1204dc508afb9a329020b2727dba6a44bebe34cd14e8877`  
		Last Modified: Wed, 04 Jan 2023 18:52:34 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6312be1510c392185507fefbf396b5fe2346e95bc93ab11fc04084e842ee0507`  
		Last Modified: Wed, 04 Jan 2023 18:52:34 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
