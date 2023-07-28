<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.19`](#emqx4419)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.26`](#emqx5026)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.2`](#emqx512)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:e3a6b7849fa4118ed412440db5f9fafeed48f87792cda9b1db11dabd0f2f7044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:fc50beecaa7b5c1e46d8f8bfc8cbbb488338b66aa4bcebc668db86420c66a274
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81431006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3bcc2f5087e2da0565a5db36c800051b3cfad79f834da16862329e41b4a2b7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:59:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:59:58 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Fri, 28 Jul 2023 00:59:58 GMT
ENV EMQX_VERSION=4.4.19
# Fri, 28 Jul 2023 00:59:58 GMT
ENV OTP=otp24.3.4.2-1
# Fri, 28 Jul 2023 01:00:04 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="bf4192c64c9006733b30f96fe99506a0a3af115c7073995a044cc0e60230675e"; fi;     if [ ${arch} = "arm64" ]; then sha256="7cd27d5112380fd4d81029b10ba862a050b0bba8af1eb90aac669189fc3053c0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$(sha256sum $pkg)";     echo "$sha256 *$pkg" | sha256sum -c;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 28 Jul 2023 01:00:04 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:04 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:04 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:04 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 28 Jul 2023 01:00:05 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:05 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e690ff3367f4d3d3d39a37f40fdf863ae19ae3695fd90f42378f95d7c177305`  
		Last Modified: Fri, 28 Jul 2023 01:00:47 GMT  
		Size: 2.6 MB (2569629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39372de4932c8edd554c7282e088f4a7dbe87e9c95f62bb6ae7e40f16629a6b6`  
		Last Modified: Fri, 28 Jul 2023 01:00:47 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6238515153ee9a756e508b5fdbe8e7f35bfd039c91baedba8531a446c9ad71c7`  
		Last Modified: Fri, 28 Jul 2023 01:00:52 GMT  
		Size: 47.4 MB (47438555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f7909d008f4712e46f7ab113b9632d2c4831fd5fe2816b2395320738625d04`  
		Last Modified: Fri, 28 Jul 2023 01:00:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a9248efad561f6b833ebacbedf28b5e25430d7246a906d41861cafd1e1ec68ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72845253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80069bbe8b69c53f5008a9f33affb0176c3d902fa45759b92bb8c8a23036632`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Thu, 06 Jul 2023 21:39:26 GMT
ENV EMQX_VERSION=4.4.19
# Thu, 06 Jul 2023 21:39:26 GMT
ENV OTP=otp24.3.4.2-1
# Thu, 06 Jul 2023 21:39:29 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="bf4192c64c9006733b30f96fe99506a0a3af115c7073995a044cc0e60230675e"; fi;     if [ ${arch} = "arm64" ]; then sha256="7cd27d5112380fd4d81029b10ba862a050b0bba8af1eb90aac669189fc3053c0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$(sha256sum $pkg)";     echo "$sha256 *$pkg" | sha256sum -c;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Thu, 06 Jul 2023 21:39:30 GMT
WORKDIR /opt/emqx
# Thu, 06 Jul 2023 21:39:30 GMT
USER emqx
# Thu, 06 Jul 2023 21:39:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 06 Jul 2023 21:39:31 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Thu, 06 Jul 2023 21:39:31 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Thu, 06 Jul 2023 21:39:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 06 Jul 2023 21:39:31 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1428b80937a0eb55c8466779cec4bcf7e31bdcc4fc66b763448cf9d131563`  
		Last Modified: Tue, 04 Jul 2023 03:03:50 GMT  
		Size: 2.6 MB (2559426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa00861c721843ae490a68a90f1db04218b5131cb6b2d6d39618973618f3da3`  
		Last Modified: Tue, 04 Jul 2023 03:03:49 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92be73299f3fbd6f630b7fd29adb355fe1bd1b77557870a88683610b34c7a8ff`  
		Last Modified: Thu, 06 Jul 2023 21:39:55 GMT  
		Size: 40.2 MB (40217654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c555c2079b356e8e46973c42652cd100382b54e914992c25f297321ad15d659`  
		Last Modified: Thu, 06 Jul 2023 21:39:52 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:e3a6b7849fa4118ed412440db5f9fafeed48f87792cda9b1db11dabd0f2f7044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:fc50beecaa7b5c1e46d8f8bfc8cbbb488338b66aa4bcebc668db86420c66a274
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81431006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3bcc2f5087e2da0565a5db36c800051b3cfad79f834da16862329e41b4a2b7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:59:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:59:58 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Fri, 28 Jul 2023 00:59:58 GMT
ENV EMQX_VERSION=4.4.19
# Fri, 28 Jul 2023 00:59:58 GMT
ENV OTP=otp24.3.4.2-1
# Fri, 28 Jul 2023 01:00:04 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="bf4192c64c9006733b30f96fe99506a0a3af115c7073995a044cc0e60230675e"; fi;     if [ ${arch} = "arm64" ]; then sha256="7cd27d5112380fd4d81029b10ba862a050b0bba8af1eb90aac669189fc3053c0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$(sha256sum $pkg)";     echo "$sha256 *$pkg" | sha256sum -c;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 28 Jul 2023 01:00:04 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:04 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:04 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:04 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 28 Jul 2023 01:00:05 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:05 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e690ff3367f4d3d3d39a37f40fdf863ae19ae3695fd90f42378f95d7c177305`  
		Last Modified: Fri, 28 Jul 2023 01:00:47 GMT  
		Size: 2.6 MB (2569629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39372de4932c8edd554c7282e088f4a7dbe87e9c95f62bb6ae7e40f16629a6b6`  
		Last Modified: Fri, 28 Jul 2023 01:00:47 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6238515153ee9a756e508b5fdbe8e7f35bfd039c91baedba8531a446c9ad71c7`  
		Last Modified: Fri, 28 Jul 2023 01:00:52 GMT  
		Size: 47.4 MB (47438555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f7909d008f4712e46f7ab113b9632d2c4831fd5fe2816b2395320738625d04`  
		Last Modified: Fri, 28 Jul 2023 01:00:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a9248efad561f6b833ebacbedf28b5e25430d7246a906d41861cafd1e1ec68ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72845253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80069bbe8b69c53f5008a9f33affb0176c3d902fa45759b92bb8c8a23036632`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Thu, 06 Jul 2023 21:39:26 GMT
ENV EMQX_VERSION=4.4.19
# Thu, 06 Jul 2023 21:39:26 GMT
ENV OTP=otp24.3.4.2-1
# Thu, 06 Jul 2023 21:39:29 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="bf4192c64c9006733b30f96fe99506a0a3af115c7073995a044cc0e60230675e"; fi;     if [ ${arch} = "arm64" ]; then sha256="7cd27d5112380fd4d81029b10ba862a050b0bba8af1eb90aac669189fc3053c0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$(sha256sum $pkg)";     echo "$sha256 *$pkg" | sha256sum -c;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Thu, 06 Jul 2023 21:39:30 GMT
WORKDIR /opt/emqx
# Thu, 06 Jul 2023 21:39:30 GMT
USER emqx
# Thu, 06 Jul 2023 21:39:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 06 Jul 2023 21:39:31 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Thu, 06 Jul 2023 21:39:31 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Thu, 06 Jul 2023 21:39:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 06 Jul 2023 21:39:31 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1428b80937a0eb55c8466779cec4bcf7e31bdcc4fc66b763448cf9d131563`  
		Last Modified: Tue, 04 Jul 2023 03:03:50 GMT  
		Size: 2.6 MB (2559426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa00861c721843ae490a68a90f1db04218b5131cb6b2d6d39618973618f3da3`  
		Last Modified: Tue, 04 Jul 2023 03:03:49 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92be73299f3fbd6f630b7fd29adb355fe1bd1b77557870a88683610b34c7a8ff`  
		Last Modified: Thu, 06 Jul 2023 21:39:55 GMT  
		Size: 40.2 MB (40217654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c555c2079b356e8e46973c42652cd100382b54e914992c25f297321ad15d659`  
		Last Modified: Thu, 06 Jul 2023 21:39:52 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.19`

```console
$ docker pull emqx@sha256:e3a6b7849fa4118ed412440db5f9fafeed48f87792cda9b1db11dabd0f2f7044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.19` - linux; amd64

```console
$ docker pull emqx@sha256:fc50beecaa7b5c1e46d8f8bfc8cbbb488338b66aa4bcebc668db86420c66a274
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81431006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3bcc2f5087e2da0565a5db36c800051b3cfad79f834da16862329e41b4a2b7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:59:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:59:58 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Fri, 28 Jul 2023 00:59:58 GMT
ENV EMQX_VERSION=4.4.19
# Fri, 28 Jul 2023 00:59:58 GMT
ENV OTP=otp24.3.4.2-1
# Fri, 28 Jul 2023 01:00:04 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="bf4192c64c9006733b30f96fe99506a0a3af115c7073995a044cc0e60230675e"; fi;     if [ ${arch} = "arm64" ]; then sha256="7cd27d5112380fd4d81029b10ba862a050b0bba8af1eb90aac669189fc3053c0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$(sha256sum $pkg)";     echo "$sha256 *$pkg" | sha256sum -c;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 28 Jul 2023 01:00:04 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:04 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:04 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:04 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 28 Jul 2023 01:00:05 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:05 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e690ff3367f4d3d3d39a37f40fdf863ae19ae3695fd90f42378f95d7c177305`  
		Last Modified: Fri, 28 Jul 2023 01:00:47 GMT  
		Size: 2.6 MB (2569629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39372de4932c8edd554c7282e088f4a7dbe87e9c95f62bb6ae7e40f16629a6b6`  
		Last Modified: Fri, 28 Jul 2023 01:00:47 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6238515153ee9a756e508b5fdbe8e7f35bfd039c91baedba8531a446c9ad71c7`  
		Last Modified: Fri, 28 Jul 2023 01:00:52 GMT  
		Size: 47.4 MB (47438555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f7909d008f4712e46f7ab113b9632d2c4831fd5fe2816b2395320738625d04`  
		Last Modified: Fri, 28 Jul 2023 01:00:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.19` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a9248efad561f6b833ebacbedf28b5e25430d7246a906d41861cafd1e1ec68ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72845253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80069bbe8b69c53f5008a9f33affb0176c3d902fa45759b92bb8c8a23036632`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Thu, 06 Jul 2023 21:39:26 GMT
ENV EMQX_VERSION=4.4.19
# Thu, 06 Jul 2023 21:39:26 GMT
ENV OTP=otp24.3.4.2-1
# Thu, 06 Jul 2023 21:39:29 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="bf4192c64c9006733b30f96fe99506a0a3af115c7073995a044cc0e60230675e"; fi;     if [ ${arch} = "arm64" ]; then sha256="7cd27d5112380fd4d81029b10ba862a050b0bba8af1eb90aac669189fc3053c0"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$(sha256sum $pkg)";     echo "$sha256 *$pkg" | sha256sum -c;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Thu, 06 Jul 2023 21:39:30 GMT
WORKDIR /opt/emqx
# Thu, 06 Jul 2023 21:39:30 GMT
USER emqx
# Thu, 06 Jul 2023 21:39:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 06 Jul 2023 21:39:31 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Thu, 06 Jul 2023 21:39:31 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Thu, 06 Jul 2023 21:39:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 06 Jul 2023 21:39:31 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1428b80937a0eb55c8466779cec4bcf7e31bdcc4fc66b763448cf9d131563`  
		Last Modified: Tue, 04 Jul 2023 03:03:50 GMT  
		Size: 2.6 MB (2559426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa00861c721843ae490a68a90f1db04218b5131cb6b2d6d39618973618f3da3`  
		Last Modified: Tue, 04 Jul 2023 03:03:49 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92be73299f3fbd6f630b7fd29adb355fe1bd1b77557870a88683610b34c7a8ff`  
		Last Modified: Thu, 06 Jul 2023 21:39:55 GMT  
		Size: 40.2 MB (40217654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c555c2079b356e8e46973c42652cd100382b54e914992c25f297321ad15d659`  
		Last Modified: Thu, 06 Jul 2023 21:39:52 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:5fab16d919b81d118ef1988b9fa9d475e79a5f75bf181febd31538d4f9ed51d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:22c80fc187af5e905971c228f5249c7e890bf33c0226671b097b25699a67b147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100541550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd13511aef47b4507981a841ff223065fc6ba8d475a51bd3bf7aa566309d66`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:00:12 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:00:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 28 Jul 2023 01:00:24 GMT
ENV EMQX_VERSION=5.1.2
# Fri, 28 Jul 2023 01:00:24 GMT
ENV AMD64_SHA256=bd34a8cfcd816305b4fc8bfb67fb8a0a29dcf7bd2e391e79534bf7d94d62ffcd
# Fri, 28 Jul 2023 01:00:25 GMT
ENV ARM64_SHA256=02d281020403f55f9d5eac5a2ffbdaebc888aa8e4b92fce847f23541f2b0eae5
# Fri, 28 Jul 2023 01:00:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 28 Jul 2023 01:00:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Fri, 28 Jul 2023 01:00:32 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:32 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:32 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 28 Jul 2023 01:00:32 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aae0cd767678d99b5128cb9f0b9f0d533d60f80be20eeda6f6530c35a813613`  
		Last Modified: Fri, 28 Jul 2023 01:01:03 GMT  
		Size: 3.0 MB (2987830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bde007415e9cca4e319dea3b886b7d723309116b3ba73372e0de710d2b6b068`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653821671e5a185406df546f8943340f6769ab3efa9290fe421be10b1fc764f8`  
		Last Modified: Fri, 28 Jul 2023 01:01:27 GMT  
		Size: 66.1 MB (66131105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cd8f9966de08a13a3fdf9adac440a9019f879b9bede5c9ae0b5725ff410c26`  
		Last Modified: Fri, 28 Jul 2023 01:01:20 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b79f2f728a453fa3ca78f59039c28fc4c90b254b15b94168cf6ccc9e0b289814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90839289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b25387bf3eaec5fbcdda3aa151b52358ebbe68464fc98222b11dd19097cb5e0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 24 Jul 2023 22:46:08 GMT
ENV EMQX_VERSION=5.1.2
# Mon, 24 Jul 2023 22:46:08 GMT
ENV AMD64_SHA256=bd34a8cfcd816305b4fc8bfb67fb8a0a29dcf7bd2e391e79534bf7d94d62ffcd
# Mon, 24 Jul 2023 22:46:08 GMT
ENV ARM64_SHA256=02d281020403f55f9d5eac5a2ffbdaebc888aa8e4b92fce847f23541f2b0eae5
# Mon, 24 Jul 2023 22:46:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 24 Jul 2023 22:46:15 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Mon, 24 Jul 2023 22:46:15 GMT
WORKDIR /opt/emqx
# Mon, 24 Jul 2023 22:46:15 GMT
USER emqx
# Mon, 24 Jul 2023 22:46:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 24 Jul 2023 22:46:15 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 24 Jul 2023 22:46:16 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 24 Jul 2023 22:46:16 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 24 Jul 2023 22:46:16 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3359f1269332e2bb900bcac8dfcdd7e02d8ad7aaa28811e10b1b939f673a9a6`  
		Last Modified: Mon, 24 Jul 2023 22:46:34 GMT  
		Size: 57.8 MB (57768247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd7972d2bafd3d78b2df6f58a44aa6d8846b547fa161ac6c05099df4da81c25`  
		Last Modified: Mon, 24 Jul 2023 22:46:29 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:86cb5b6a4419464d2f53269cbb11e4e51202b35d5c17f3d1f2a8b8c61a4489e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:fc52de5e495b2127918496f4279ce1175fa131ce3dd3f104ee6589565a02dd34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101982317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dd67ffa630f220137ee6f5f73b65717f8a54256a8e063c705ffcfc115aed6c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:00:12 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:00:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 28 Jul 2023 01:00:13 GMT
ENV EMQX_VERSION=5.0.26
# Fri, 28 Jul 2023 01:00:13 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Fri, 28 Jul 2023 01:00:13 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Fri, 28 Jul 2023 01:00:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 28 Jul 2023 01:00:19 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 28 Jul 2023 01:00:20 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:20 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:20 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 28 Jul 2023 01:00:20 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aae0cd767678d99b5128cb9f0b9f0d533d60f80be20eeda6f6530c35a813613`  
		Last Modified: Fri, 28 Jul 2023 01:01:03 GMT  
		Size: 3.0 MB (2987830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bde007415e9cca4e319dea3b886b7d723309116b3ba73372e0de710d2b6b068`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788aa6e14f2bb644a8ea6308bc63a5293c7100c1cf56c89d166f0fbafc7f452`  
		Last Modified: Fri, 28 Jul 2023 01:01:11 GMT  
		Size: 67.6 MB (67571870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0def11967b7af57de71d52d148a123356502d2957e2fa39a551edd11526ae9dc`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0abdd21e8a6b3206455cb733eca21c22695b7dc06a98d3a4de5eb999537b0195
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93060437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db90f1f3fab83ce999d6472a64971ca463afb82097d6b4cdb5da98a3c2f28c0d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 04 Jul 2023 03:03:22 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 04 Jul 2023 03:03:22 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 04 Jul 2023 03:03:22 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 04 Jul 2023 03:03:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Jul 2023 03:03:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 04 Jul 2023 03:03:28 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:28 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 04 Jul 2023 03:03:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf20fcfbb7660480c1e5425d2d670e3fc48e00264da9d9a5b0eb282e2472df6`  
		Last Modified: Tue, 04 Jul 2023 03:04:08 GMT  
		Size: 60.0 MB (59989394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03deeecf9242891f89e9ebbde2e0197c04be91ee39569bfcd63a6a3336b20801`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.26`

```console
$ docker pull emqx@sha256:86cb5b6a4419464d2f53269cbb11e4e51202b35d5c17f3d1f2a8b8c61a4489e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.26` - linux; amd64

```console
$ docker pull emqx@sha256:fc52de5e495b2127918496f4279ce1175fa131ce3dd3f104ee6589565a02dd34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101982317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dd67ffa630f220137ee6f5f73b65717f8a54256a8e063c705ffcfc115aed6c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:00:12 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:00:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 28 Jul 2023 01:00:13 GMT
ENV EMQX_VERSION=5.0.26
# Fri, 28 Jul 2023 01:00:13 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Fri, 28 Jul 2023 01:00:13 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Fri, 28 Jul 2023 01:00:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 28 Jul 2023 01:00:19 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 28 Jul 2023 01:00:20 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:20 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:20 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 28 Jul 2023 01:00:20 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aae0cd767678d99b5128cb9f0b9f0d533d60f80be20eeda6f6530c35a813613`  
		Last Modified: Fri, 28 Jul 2023 01:01:03 GMT  
		Size: 3.0 MB (2987830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bde007415e9cca4e319dea3b886b7d723309116b3ba73372e0de710d2b6b068`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788aa6e14f2bb644a8ea6308bc63a5293c7100c1cf56c89d166f0fbafc7f452`  
		Last Modified: Fri, 28 Jul 2023 01:01:11 GMT  
		Size: 67.6 MB (67571870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0def11967b7af57de71d52d148a123356502d2957e2fa39a551edd11526ae9dc`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.26` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0abdd21e8a6b3206455cb733eca21c22695b7dc06a98d3a4de5eb999537b0195
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93060437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db90f1f3fab83ce999d6472a64971ca463afb82097d6b4cdb5da98a3c2f28c0d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 04 Jul 2023 03:03:22 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 04 Jul 2023 03:03:22 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 04 Jul 2023 03:03:22 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 04 Jul 2023 03:03:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Jul 2023 03:03:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 04 Jul 2023 03:03:28 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:28 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 04 Jul 2023 03:03:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf20fcfbb7660480c1e5425d2d670e3fc48e00264da9d9a5b0eb282e2472df6`  
		Last Modified: Tue, 04 Jul 2023 03:04:08 GMT  
		Size: 60.0 MB (59989394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03deeecf9242891f89e9ebbde2e0197c04be91ee39569bfcd63a6a3336b20801`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:5fab16d919b81d118ef1988b9fa9d475e79a5f75bf181febd31538d4f9ed51d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:22c80fc187af5e905971c228f5249c7e890bf33c0226671b097b25699a67b147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100541550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd13511aef47b4507981a841ff223065fc6ba8d475a51bd3bf7aa566309d66`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:00:12 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:00:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 28 Jul 2023 01:00:24 GMT
ENV EMQX_VERSION=5.1.2
# Fri, 28 Jul 2023 01:00:24 GMT
ENV AMD64_SHA256=bd34a8cfcd816305b4fc8bfb67fb8a0a29dcf7bd2e391e79534bf7d94d62ffcd
# Fri, 28 Jul 2023 01:00:25 GMT
ENV ARM64_SHA256=02d281020403f55f9d5eac5a2ffbdaebc888aa8e4b92fce847f23541f2b0eae5
# Fri, 28 Jul 2023 01:00:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 28 Jul 2023 01:00:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Fri, 28 Jul 2023 01:00:32 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:32 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:32 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 28 Jul 2023 01:00:32 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aae0cd767678d99b5128cb9f0b9f0d533d60f80be20eeda6f6530c35a813613`  
		Last Modified: Fri, 28 Jul 2023 01:01:03 GMT  
		Size: 3.0 MB (2987830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bde007415e9cca4e319dea3b886b7d723309116b3ba73372e0de710d2b6b068`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653821671e5a185406df546f8943340f6769ab3efa9290fe421be10b1fc764f8`  
		Last Modified: Fri, 28 Jul 2023 01:01:27 GMT  
		Size: 66.1 MB (66131105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cd8f9966de08a13a3fdf9adac440a9019f879b9bede5c9ae0b5725ff410c26`  
		Last Modified: Fri, 28 Jul 2023 01:01:20 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b79f2f728a453fa3ca78f59039c28fc4c90b254b15b94168cf6ccc9e0b289814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90839289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b25387bf3eaec5fbcdda3aa151b52358ebbe68464fc98222b11dd19097cb5e0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 24 Jul 2023 22:46:08 GMT
ENV EMQX_VERSION=5.1.2
# Mon, 24 Jul 2023 22:46:08 GMT
ENV AMD64_SHA256=bd34a8cfcd816305b4fc8bfb67fb8a0a29dcf7bd2e391e79534bf7d94d62ffcd
# Mon, 24 Jul 2023 22:46:08 GMT
ENV ARM64_SHA256=02d281020403f55f9d5eac5a2ffbdaebc888aa8e4b92fce847f23541f2b0eae5
# Mon, 24 Jul 2023 22:46:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 24 Jul 2023 22:46:15 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Mon, 24 Jul 2023 22:46:15 GMT
WORKDIR /opt/emqx
# Mon, 24 Jul 2023 22:46:15 GMT
USER emqx
# Mon, 24 Jul 2023 22:46:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 24 Jul 2023 22:46:15 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 24 Jul 2023 22:46:16 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 24 Jul 2023 22:46:16 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 24 Jul 2023 22:46:16 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3359f1269332e2bb900bcac8dfcdd7e02d8ad7aaa28811e10b1b939f673a9a6`  
		Last Modified: Mon, 24 Jul 2023 22:46:34 GMT  
		Size: 57.8 MB (57768247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd7972d2bafd3d78b2df6f58a44aa6d8846b547fa161ac6c05099df4da81c25`  
		Last Modified: Mon, 24 Jul 2023 22:46:29 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.2`

```console
$ docker pull emqx@sha256:5fab16d919b81d118ef1988b9fa9d475e79a5f75bf181febd31538d4f9ed51d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.2` - linux; amd64

```console
$ docker pull emqx@sha256:22c80fc187af5e905971c228f5249c7e890bf33c0226671b097b25699a67b147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100541550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd13511aef47b4507981a841ff223065fc6ba8d475a51bd3bf7aa566309d66`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:00:12 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:00:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 28 Jul 2023 01:00:24 GMT
ENV EMQX_VERSION=5.1.2
# Fri, 28 Jul 2023 01:00:24 GMT
ENV AMD64_SHA256=bd34a8cfcd816305b4fc8bfb67fb8a0a29dcf7bd2e391e79534bf7d94d62ffcd
# Fri, 28 Jul 2023 01:00:25 GMT
ENV ARM64_SHA256=02d281020403f55f9d5eac5a2ffbdaebc888aa8e4b92fce847f23541f2b0eae5
# Fri, 28 Jul 2023 01:00:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 28 Jul 2023 01:00:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Fri, 28 Jul 2023 01:00:32 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:32 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:32 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 28 Jul 2023 01:00:32 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aae0cd767678d99b5128cb9f0b9f0d533d60f80be20eeda6f6530c35a813613`  
		Last Modified: Fri, 28 Jul 2023 01:01:03 GMT  
		Size: 3.0 MB (2987830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bde007415e9cca4e319dea3b886b7d723309116b3ba73372e0de710d2b6b068`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653821671e5a185406df546f8943340f6769ab3efa9290fe421be10b1fc764f8`  
		Last Modified: Fri, 28 Jul 2023 01:01:27 GMT  
		Size: 66.1 MB (66131105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cd8f9966de08a13a3fdf9adac440a9019f879b9bede5c9ae0b5725ff410c26`  
		Last Modified: Fri, 28 Jul 2023 01:01:20 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b79f2f728a453fa3ca78f59039c28fc4c90b254b15b94168cf6ccc9e0b289814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90839289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b25387bf3eaec5fbcdda3aa151b52358ebbe68464fc98222b11dd19097cb5e0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 24 Jul 2023 22:46:08 GMT
ENV EMQX_VERSION=5.1.2
# Mon, 24 Jul 2023 22:46:08 GMT
ENV AMD64_SHA256=bd34a8cfcd816305b4fc8bfb67fb8a0a29dcf7bd2e391e79534bf7d94d62ffcd
# Mon, 24 Jul 2023 22:46:08 GMT
ENV ARM64_SHA256=02d281020403f55f9d5eac5a2ffbdaebc888aa8e4b92fce847f23541f2b0eae5
# Mon, 24 Jul 2023 22:46:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 24 Jul 2023 22:46:15 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Mon, 24 Jul 2023 22:46:15 GMT
WORKDIR /opt/emqx
# Mon, 24 Jul 2023 22:46:15 GMT
USER emqx
# Mon, 24 Jul 2023 22:46:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 24 Jul 2023 22:46:15 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 24 Jul 2023 22:46:16 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 24 Jul 2023 22:46:16 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 24 Jul 2023 22:46:16 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3359f1269332e2bb900bcac8dfcdd7e02d8ad7aaa28811e10b1b939f673a9a6`  
		Last Modified: Mon, 24 Jul 2023 22:46:34 GMT  
		Size: 57.8 MB (57768247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd7972d2bafd3d78b2df6f58a44aa6d8846b547fa161ac6c05099df4da81c25`  
		Last Modified: Mon, 24 Jul 2023 22:46:29 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:5fab16d919b81d118ef1988b9fa9d475e79a5f75bf181febd31538d4f9ed51d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:22c80fc187af5e905971c228f5249c7e890bf33c0226671b097b25699a67b147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100541550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd13511aef47b4507981a841ff223065fc6ba8d475a51bd3bf7aa566309d66`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:00:12 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:00:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 28 Jul 2023 01:00:24 GMT
ENV EMQX_VERSION=5.1.2
# Fri, 28 Jul 2023 01:00:24 GMT
ENV AMD64_SHA256=bd34a8cfcd816305b4fc8bfb67fb8a0a29dcf7bd2e391e79534bf7d94d62ffcd
# Fri, 28 Jul 2023 01:00:25 GMT
ENV ARM64_SHA256=02d281020403f55f9d5eac5a2ffbdaebc888aa8e4b92fce847f23541f2b0eae5
# Fri, 28 Jul 2023 01:00:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 28 Jul 2023 01:00:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Fri, 28 Jul 2023 01:00:32 GMT
WORKDIR /opt/emqx
# Fri, 28 Jul 2023 01:00:32 GMT
USER emqx
# Fri, 28 Jul 2023 01:00:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 28 Jul 2023 01:00:32 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 28 Jul 2023 01:00:32 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 28 Jul 2023 01:00:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:00:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aae0cd767678d99b5128cb9f0b9f0d533d60f80be20eeda6f6530c35a813613`  
		Last Modified: Fri, 28 Jul 2023 01:01:03 GMT  
		Size: 3.0 MB (2987830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bde007415e9cca4e319dea3b886b7d723309116b3ba73372e0de710d2b6b068`  
		Last Modified: Fri, 28 Jul 2023 01:01:02 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653821671e5a185406df546f8943340f6769ab3efa9290fe421be10b1fc764f8`  
		Last Modified: Fri, 28 Jul 2023 01:01:27 GMT  
		Size: 66.1 MB (66131105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cd8f9966de08a13a3fdf9adac440a9019f879b9bede5c9ae0b5725ff410c26`  
		Last Modified: Fri, 28 Jul 2023 01:01:20 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b79f2f728a453fa3ca78f59039c28fc4c90b254b15b94168cf6ccc9e0b289814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90839289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b25387bf3eaec5fbcdda3aa151b52358ebbe68464fc98222b11dd19097cb5e0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Mon, 24 Jul 2023 22:46:08 GMT
ENV EMQX_VERSION=5.1.2
# Mon, 24 Jul 2023 22:46:08 GMT
ENV AMD64_SHA256=bd34a8cfcd816305b4fc8bfb67fb8a0a29dcf7bd2e391e79534bf7d94d62ffcd
# Mon, 24 Jul 2023 22:46:08 GMT
ENV ARM64_SHA256=02d281020403f55f9d5eac5a2ffbdaebc888aa8e4b92fce847f23541f2b0eae5
# Mon, 24 Jul 2023 22:46:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 24 Jul 2023 22:46:15 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Mon, 24 Jul 2023 22:46:15 GMT
WORKDIR /opt/emqx
# Mon, 24 Jul 2023 22:46:15 GMT
USER emqx
# Mon, 24 Jul 2023 22:46:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 24 Jul 2023 22:46:15 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Mon, 24 Jul 2023 22:46:16 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 24 Jul 2023 22:46:16 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 24 Jul 2023 22:46:16 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3359f1269332e2bb900bcac8dfcdd7e02d8ad7aaa28811e10b1b939f673a9a6`  
		Last Modified: Mon, 24 Jul 2023 22:46:34 GMT  
		Size: 57.8 MB (57768247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd7972d2bafd3d78b2df6f58a44aa6d8846b547fa161ac6c05099df4da81c25`  
		Last Modified: Mon, 24 Jul 2023 22:46:29 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
