## `clojure:temurin-19-boot-bullseye`

```console
$ docker pull clojure@sha256:310ce6194a2aed424b69a9f2a95343e636eb044fdf2d82a2c6879cbfd05a117f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cdfbe7bfd57c47465e7cd416e0109fa935cbdd09c4ecad6b2a69e9ae3591432d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317342129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de63c94dd43e15ab8b705614f1049030dbb2f0d03e772b8f4664fb4ea57efdc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:05 GMT
ADD file:b03d13d345c29f69557f410c8504e748226756d1f48e5abdb63cd40179b2640c in / 
# Thu, 09 Feb 2023 03:20:05 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:22:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Feb 2023 09:31:09 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Thu, 09 Feb 2023 09:31:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 09:31:11 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 09 Feb 2023 09:31:11 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 09 Feb 2023 09:31:11 GMT
WORKDIR /tmp
# Thu, 09 Feb 2023 09:31:17 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 09 Feb 2023 09:31:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Feb 2023 09:31:17 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 09 Feb 2023 09:31:35 GMT
RUN boot
# Thu, 09 Feb 2023 09:31:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 09 Feb 2023 09:31:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Feb 2023 09:31:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e4aec178e0864db93a6f97a20bde3445871a4562c1801185eca1238d3a0e80d`  
		Last Modified: Thu, 09 Feb 2023 03:24:47 GMT  
		Size: 55.0 MB (55046771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441046777b829253c9900fed7834e1437d44d485f4ec90904dc51bc5aac05148`  
		Last Modified: Thu, 09 Feb 2023 09:42:23 GMT  
		Size: 201.1 MB (201112949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83e8d70b4ddc7fa2baeb223f53b510152bc8a430e87f8ae7283d651780b370f`  
		Last Modified: Thu, 09 Feb 2023 09:42:08 GMT  
		Size: 2.4 MB (2361683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce97ae42bd76b200ed6a250b45956055d4e90d7dcc3d22cde60fc5b4adc425e`  
		Last Modified: Thu, 09 Feb 2023 09:42:11 GMT  
		Size: 58.8 MB (58820325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edccb83e2efea5b42ae6e4e389186faac15c41a75f6ff307a42bad5d33bf5e59`  
		Last Modified: Thu, 09 Feb 2023 09:42:08 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e60f2294757013ed8e3f8859ca3dfd264a2d03623a58c2877215ca618d42e861
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314730199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2adb7918bfefe1afc277360bd6f4738580cc9c1f037332794a791f917f55d15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:09:13 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:09:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:09:17 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:09:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:09:17 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:09:22 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:09:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:09:22 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:09:39 GMT
RUN boot
# Wed, 01 Mar 2023 03:09:39 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 03:09:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 03:09:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f14b17f40d43b36c3ca31112958858ecb243428662f3cf865bcfd47ff1cf7c3`  
		Last Modified: Wed, 01 Mar 2023 03:19:11 GMT  
		Size: 199.9 MB (199855198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e5ca17536fd9194f5c18c3b1e9941b9469f82cc49fade200aabd23a3b471f6`  
		Last Modified: Wed, 01 Mar 2023 03:18:59 GMT  
		Size: 2.4 MB (2351009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cfcef5c1deb8dca1dd939a15f11c3f5581c504379a1926fbf58654aea2497e`  
		Last Modified: Wed, 01 Mar 2023 03:19:02 GMT  
		Size: 58.8 MB (58820378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966c0431db5929c9cdcb91d09e819b2dd8398145a689d50f2c24cbaacecaadc`  
		Last Modified: Wed, 01 Mar 2023 03:18:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
