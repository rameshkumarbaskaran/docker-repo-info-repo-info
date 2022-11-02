## `clojure:temurin-17-tools-deps-1.11.1.1182-bullseye`

```console
$ docker pull clojure@sha256:2f86f22139fe85f0d2c42652a1c821408b81eb1ebfe053220174c60746549974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1182-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:16592d191a76ecc3d6f21f241aa0e19495b3ad0afb7c11b1bab99f57263d4ab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294485726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cf033b4979edf107e53d3148fda35ab1e3e4ba54fe7cb03fd69b10e1966310`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:14:51 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:14:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:17:16 GMT
ENV CLOJURE_VERSION=1.11.1.1182
# Wed, 02 Nov 2022 20:17:16 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:17:31 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0e80041419bb91e142e2e8683e4dad6faf79958b603bb63b2a93bdd62c2a4f14 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 02 Nov 2022 20:17:32 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Nov 2022 20:17:32 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:17:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:17:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a743048e6b028bb91e927d7a70b42b7aa572cabf53bf650a7aa0bc002e2463`  
		Last Modified: Wed, 02 Nov 2022 20:27:22 GMT  
		Size: 192.1 MB (192137487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103c7f956ba0ecdd963f7b7560dfb551a794b7c8ee260b1b55e2988c827c4c41`  
		Last Modified: Wed, 02 Nov 2022 20:29:24 GMT  
		Size: 47.3 MB (47300890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b1ec14d7e72699af7e8415c080711bdd3ff215fdd8898f2d5f4a8dcdd95a7`  
		Last Modified: Wed, 02 Nov 2022 20:29:19 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3910ff4559e6134d039bd7bc1e5f3d0fec5bb3094800f37e37a76776aad946c`  
		Last Modified: Wed, 02 Nov 2022 20:29:19 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1182-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fbae5aa0f58f438c8d92c9d61c5a8d85df8c16eb2416ff69800d413d0148dfe6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291901408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3de39c5fd4ef59cbaa8adf23789748b57741076787d0da26c8d7b909cfb3ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:08 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:50:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:52:19 GMT
ENV CLOJURE_VERSION=1.11.1.1182
# Wed, 02 Nov 2022 20:52:19 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:52:30 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0e80041419bb91e142e2e8683e4dad6faf79958b603bb63b2a93bdd62c2a4f14 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 02 Nov 2022 20:52:31 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Nov 2022 20:52:31 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:52:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:52:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4deacd3ca10c3fa2537fe32ec939ce8fdafac62c9fc22abfa01f8f33e869e008`  
		Last Modified: Wed, 02 Nov 2022 21:01:00 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b50f4da5dd4091e679b1444afb6c057b7843a0fac96e328153f0c532c9fc885`  
		Last Modified: Wed, 02 Nov 2022 21:03:07 GMT  
		Size: 47.3 MB (47294330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b97fff9cb69de747327bdde74f5409c2200485064c707da66eb78d82132abec`  
		Last Modified: Wed, 02 Nov 2022 21:03:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde0678e8f9bdc0ac83a4e1bf0d4b8e041f91e3a6a1cef85118b1f0d1c5f64fb`  
		Last Modified: Wed, 02 Nov 2022 21:03:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
