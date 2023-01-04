## `clojure:temurin-17-tools-deps-1.11.1.1208-bullseye`

```console
$ docker pull clojure@sha256:afc9ab20a55f76f53b12c9025d30823ec24493a57ec7bd28dad88ee3857b55e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1208-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:25c78df5f36360c75a57e0e50d228430f5cb0adf7b142f1185b58bb8a6a685b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.3 MB (319315242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c1bec55010e8e586c0c9877139b2d889da317fa5e9b2b08ccf1b8f7221b30d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:21 GMT
ADD file:c13b430c8699df107ffd9ea5230b92238bc037a8e1cbbe35d6ab664941d575da in / 
# Wed, 21 Dec 2022 01:20:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:50:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:56:26 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 21 Dec 2022 01:56:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jan 2023 19:25:37 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 04 Jan 2023 19:25:37 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 19:25:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 04 Jan 2023 19:25:56 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 19:25:56 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 04 Jan 2023 19:25:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Jan 2023 19:25:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:32de3c850997ce03b6ff4ae8fb00b34b9d7d7f9a35bfcdb8538e22cc7b77c29d`  
		Last Modified: Wed, 21 Dec 2022 01:24:10 GMT  
		Size: 55.0 MB (55025166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85d928f7af45063c8909fd71ef1d2934126eb27a444735b74dc4b9d177542d7`  
		Last Modified: Wed, 21 Dec 2022 02:08:49 GMT  
		Size: 192.4 MB (192431250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6035a2f132db0c9340878044d7d3b77a71500745c540bc2047306c41f73d40`  
		Last Modified: Wed, 04 Jan 2023 19:34:06 GMT  
		Size: 71.9 MB (71857806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb0ca46ec1c15a529187d9ba47f84af7bb9d2181ae25cec4751ab5cbb3c0ab4`  
		Last Modified: Wed, 04 Jan 2023 19:33:57 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cddda1021f9e05ce6191ab847542b62b36a85a7d5e1fbc9f41c1463c7113ea`  
		Last Modified: Wed, 04 Jan 2023 19:33:57 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1208-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dad56720280a8a82db2bd3bdf557b4b0a1f9fcdaa3ec69c78a4ccf652bee7da1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316877285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672ad24949da6d56147792cba0f66cce451df3dcf892c9224d1c847c44eb5bd8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:40 GMT
ADD file:5bbdc914ec8ed60ac85293e88ee1aafc3f0290762e320fc86dc9d79fa201834e in / 
# Wed, 21 Dec 2022 01:39:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:18:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 02:23:13 GMT
COPY dir:533cfee1c12b6052cd1297ebc89704c8b7da6e8016c06b0e341bcec0d4934dde in /opt/java/openjdk 
# Wed, 21 Dec 2022 02:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jan 2023 18:44:44 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Wed, 04 Jan 2023 18:44:44 GMT
WORKDIR /tmp
# Wed, 04 Jan 2023 18:44:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 04 Jan 2023 18:44:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 04 Jan 2023 18:44:58 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 04 Jan 2023 18:44:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Jan 2023 18:44:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3e6129b48b69d14c5e7a5605e2b94003fb71aac82eac46b8689f5b8007af2c5`  
		Last Modified: Wed, 21 Dec 2022 01:42:49 GMT  
		Size: 53.7 MB (53681797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7590a9cfd73d6147f6887d3e0a5cb84fcb61c48a400fb999741e356bc525b005`  
		Last Modified: Wed, 21 Dec 2022 02:33:56 GMT  
		Size: 191.2 MB (191215202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a0e115ce56f55c72040bad15b00a0026f6b707c90be4a53b5565336dbd66df`  
		Last Modified: Wed, 04 Jan 2023 18:51:46 GMT  
		Size: 72.0 MB (71979267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dae2859d70ab78b5440fa851fd681d337555307ce7f8fa2d89ad533119f771d`  
		Last Modified: Wed, 04 Jan 2023 18:51:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff3e210ac821472ad2f07805cc52b2bde479cf980a1436df2cd6a09254fd73a`  
		Last Modified: Wed, 04 Jan 2023 18:51:39 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
