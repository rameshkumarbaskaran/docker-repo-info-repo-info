<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:2`](#dart2)
-	[`dart:2-sdk`](#dart2-sdk)
-	[`dart:2.15`](#dart215)
-	[`dart:2.15-sdk`](#dart215-sdk)
-	[`dart:2.15.1`](#dart2151)
-	[`dart:2.15.1-sdk`](#dart2151-sdk)
-	[`dart:2.16.0-80.1.beta`](#dart2160-801beta)
-	[`dart:2.16.0-80.1.beta-sdk`](#dart2160-801beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:2`

```console
$ docker pull dart@sha256:99d94dc835b579e004543bd86b60ee2b4c8e2864e2953b905fe944f1cdbd2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm variant v7

```console
$ docker pull dart@sha256:a8c98e81a3b99149b2624638d761f73c50bb1f0fe8635af5c965bb367dfdc9e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b6be7185ef911caf0cff5b08b0061aba7e0e9c8d4d1718d4e89fa7e85d490`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e331f648f565998a32bd4ad9477c0990e10df0d5be4d5ce06a34a8ee00e779`  
		Last Modified: Tue, 14 Dec 2021 20:01:05 GMT  
		Size: 115.2 MB (115178100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2-sdk`

```console
$ docker pull dart@sha256:99d94dc835b579e004543bd86b60ee2b4c8e2864e2953b905fe944f1cdbd2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a8c98e81a3b99149b2624638d761f73c50bb1f0fe8635af5c965bb367dfdc9e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b6be7185ef911caf0cff5b08b0061aba7e0e9c8d4d1718d4e89fa7e85d490`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e331f648f565998a32bd4ad9477c0990e10df0d5be4d5ce06a34a8ee00e779`  
		Last Modified: Tue, 14 Dec 2021 20:01:05 GMT  
		Size: 115.2 MB (115178100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.15`

```console
$ docker pull dart@sha256:99d94dc835b579e004543bd86b60ee2b4c8e2864e2953b905fe944f1cdbd2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.15` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15` - linux; arm variant v7

```console
$ docker pull dart@sha256:a8c98e81a3b99149b2624638d761f73c50bb1f0fe8635af5c965bb367dfdc9e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b6be7185ef911caf0cff5b08b0061aba7e0e9c8d4d1718d4e89fa7e85d490`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e331f648f565998a32bd4ad9477c0990e10df0d5be4d5ce06a34a8ee00e779`  
		Last Modified: Tue, 14 Dec 2021 20:01:05 GMT  
		Size: 115.2 MB (115178100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.15-sdk`

```console
$ docker pull dart@sha256:99d94dc835b579e004543bd86b60ee2b4c8e2864e2953b905fe944f1cdbd2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.15-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a8c98e81a3b99149b2624638d761f73c50bb1f0fe8635af5c965bb367dfdc9e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b6be7185ef911caf0cff5b08b0061aba7e0e9c8d4d1718d4e89fa7e85d490`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e331f648f565998a32bd4ad9477c0990e10df0d5be4d5ce06a34a8ee00e779`  
		Last Modified: Tue, 14 Dec 2021 20:01:05 GMT  
		Size: 115.2 MB (115178100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.15.1`

```console
$ docker pull dart@sha256:99d94dc835b579e004543bd86b60ee2b4c8e2864e2953b905fe944f1cdbd2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.15.1` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:a8c98e81a3b99149b2624638d761f73c50bb1f0fe8635af5c965bb367dfdc9e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b6be7185ef911caf0cff5b08b0061aba7e0e9c8d4d1718d4e89fa7e85d490`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e331f648f565998a32bd4ad9477c0990e10df0d5be4d5ce06a34a8ee00e779`  
		Last Modified: Tue, 14 Dec 2021 20:01:05 GMT  
		Size: 115.2 MB (115178100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.15.1-sdk`

```console
$ docker pull dart@sha256:99d94dc835b579e004543bd86b60ee2b4c8e2864e2953b905fe944f1cdbd2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.15.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a8c98e81a3b99149b2624638d761f73c50bb1f0fe8635af5c965bb367dfdc9e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b6be7185ef911caf0cff5b08b0061aba7e0e9c8d4d1718d4e89fa7e85d490`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e331f648f565998a32bd4ad9477c0990e10df0d5be4d5ce06a34a8ee00e779`  
		Last Modified: Tue, 14 Dec 2021 20:01:05 GMT  
		Size: 115.2 MB (115178100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16.0-80.1.beta`

```console
$ docker pull dart@sha256:8f1aa1ff313c3559750492dc030082244ceddbd26408c5aee37f50dcc84b0314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.16.0-80.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:1c24661ac875e11b2a31c7abe1f3bc81b62de5d068b18252ca2f6d3eb1e3cedf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283568777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc8cb35c3be994f9da66a4f3a3dcbf498c8437a84db891ba9e9771b4b5e413b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad35e7d39210bebff8e8cb87bda3d96226d6582f5461f9e8328f06cf2b8505d`  
		Last Modified: Tue, 21 Dec 2021 02:14:38 GMT  
		Size: 204.5 MB (204472423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.0-80.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:2ca0caeb6142655524cbd30fdd87e723ba1087866b228b9d0a8b14c09adeea37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190591078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2f1fd1166da5344ad8b24891990382956c04033e4e439627aac1acf40beeb8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:58:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad1ca0269b35ee0abf27a55d8e32e83db3c4f632ef85690b0ee9b4e4f6fb785`  
		Last Modified: Tue, 14 Dec 2021 20:03:08 GMT  
		Size: 122.1 MB (122081579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.0-80.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:91f675afe5e18731b1a27e7fd5ecd2ada05b3d2efc15e6b118c1916cb1a4ec6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200774170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b28d681a58cbf2671c746405b6e8bd9e097ae3a160496e1a2bc1a4ec44c5a3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffa4f4b83f59785e08b478d2174c33afd9211c38e35984358e40e36c1f74175`  
		Last Modified: Tue, 14 Dec 2021 20:41:38 GMT  
		Size: 123.6 MB (123580013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16.0-80.1.beta-sdk`

```console
$ docker pull dart@sha256:8f1aa1ff313c3559750492dc030082244ceddbd26408c5aee37f50dcc84b0314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.16.0-80.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1c24661ac875e11b2a31c7abe1f3bc81b62de5d068b18252ca2f6d3eb1e3cedf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283568777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc8cb35c3be994f9da66a4f3a3dcbf498c8437a84db891ba9e9771b4b5e413b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad35e7d39210bebff8e8cb87bda3d96226d6582f5461f9e8328f06cf2b8505d`  
		Last Modified: Tue, 21 Dec 2021 02:14:38 GMT  
		Size: 204.5 MB (204472423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.0-80.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2ca0caeb6142655524cbd30fdd87e723ba1087866b228b9d0a8b14c09adeea37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190591078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2f1fd1166da5344ad8b24891990382956c04033e4e439627aac1acf40beeb8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:58:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad1ca0269b35ee0abf27a55d8e32e83db3c4f632ef85690b0ee9b4e4f6fb785`  
		Last Modified: Tue, 14 Dec 2021 20:03:08 GMT  
		Size: 122.1 MB (122081579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.0-80.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:91f675afe5e18731b1a27e7fd5ecd2ada05b3d2efc15e6b118c1916cb1a4ec6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200774170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b28d681a58cbf2671c746405b6e8bd9e097ae3a160496e1a2bc1a4ec44c5a3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffa4f4b83f59785e08b478d2174c33afd9211c38e35984358e40e36c1f74175`  
		Last Modified: Tue, 14 Dec 2021 20:41:38 GMT  
		Size: 123.6 MB (123580013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:8f1aa1ff313c3559750492dc030082244ceddbd26408c5aee37f50dcc84b0314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:1c24661ac875e11b2a31c7abe1f3bc81b62de5d068b18252ca2f6d3eb1e3cedf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283568777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc8cb35c3be994f9da66a4f3a3dcbf498c8437a84db891ba9e9771b4b5e413b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad35e7d39210bebff8e8cb87bda3d96226d6582f5461f9e8328f06cf2b8505d`  
		Last Modified: Tue, 21 Dec 2021 02:14:38 GMT  
		Size: 204.5 MB (204472423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:2ca0caeb6142655524cbd30fdd87e723ba1087866b228b9d0a8b14c09adeea37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190591078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2f1fd1166da5344ad8b24891990382956c04033e4e439627aac1acf40beeb8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:58:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad1ca0269b35ee0abf27a55d8e32e83db3c4f632ef85690b0ee9b4e4f6fb785`  
		Last Modified: Tue, 14 Dec 2021 20:03:08 GMT  
		Size: 122.1 MB (122081579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:91f675afe5e18731b1a27e7fd5ecd2ada05b3d2efc15e6b118c1916cb1a4ec6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200774170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b28d681a58cbf2671c746405b6e8bd9e097ae3a160496e1a2bc1a4ec44c5a3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffa4f4b83f59785e08b478d2174c33afd9211c38e35984358e40e36c1f74175`  
		Last Modified: Tue, 14 Dec 2021 20:41:38 GMT  
		Size: 123.6 MB (123580013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:8f1aa1ff313c3559750492dc030082244ceddbd26408c5aee37f50dcc84b0314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1c24661ac875e11b2a31c7abe1f3bc81b62de5d068b18252ca2f6d3eb1e3cedf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283568777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc8cb35c3be994f9da66a4f3a3dcbf498c8437a84db891ba9e9771b4b5e413b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad35e7d39210bebff8e8cb87bda3d96226d6582f5461f9e8328f06cf2b8505d`  
		Last Modified: Tue, 21 Dec 2021 02:14:38 GMT  
		Size: 204.5 MB (204472423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2ca0caeb6142655524cbd30fdd87e723ba1087866b228b9d0a8b14c09adeea37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190591078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2f1fd1166da5344ad8b24891990382956c04033e4e439627aac1acf40beeb8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:58:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad1ca0269b35ee0abf27a55d8e32e83db3c4f632ef85690b0ee9b4e4f6fb785`  
		Last Modified: Tue, 14 Dec 2021 20:03:08 GMT  
		Size: 122.1 MB (122081579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:91f675afe5e18731b1a27e7fd5ecd2ada05b3d2efc15e6b118c1916cb1a4ec6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200774170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b28d681a58cbf2671c746405b6e8bd9e097ae3a160496e1a2bc1a4ec44c5a3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffa4f4b83f59785e08b478d2174c33afd9211c38e35984358e40e36c1f74175`  
		Last Modified: Tue, 14 Dec 2021 20:41:38 GMT  
		Size: 123.6 MB (123580013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:99d94dc835b579e004543bd86b60ee2b4c8e2864e2953b905fe944f1cdbd2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:a8c98e81a3b99149b2624638d761f73c50bb1f0fe8635af5c965bb367dfdc9e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b6be7185ef911caf0cff5b08b0061aba7e0e9c8d4d1718d4e89fa7e85d490`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e331f648f565998a32bd4ad9477c0990e10df0d5be4d5ce06a34a8ee00e779`  
		Last Modified: Tue, 14 Dec 2021 20:01:05 GMT  
		Size: 115.2 MB (115178100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:99d94dc835b579e004543bd86b60ee2b4c8e2864e2953b905fe944f1cdbd2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a8c98e81a3b99149b2624638d761f73c50bb1f0fe8635af5c965bb367dfdc9e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b6be7185ef911caf0cff5b08b0061aba7e0e9c8d4d1718d4e89fa7e85d490`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e331f648f565998a32bd4ad9477c0990e10df0d5be4d5ce06a34a8ee00e779`  
		Last Modified: Tue, 14 Dec 2021 20:01:05 GMT  
		Size: 115.2 MB (115178100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:99d94dc835b579e004543bd86b60ee2b4c8e2864e2953b905fe944f1cdbd2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:a8c98e81a3b99149b2624638d761f73c50bb1f0fe8635af5c965bb367dfdc9e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b6be7185ef911caf0cff5b08b0061aba7e0e9c8d4d1718d4e89fa7e85d490`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e331f648f565998a32bd4ad9477c0990e10df0d5be4d5ce06a34a8ee00e779`  
		Last Modified: Tue, 14 Dec 2021 20:01:05 GMT  
		Size: 115.2 MB (115178100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:99d94dc835b579e004543bd86b60ee2b4c8e2864e2953b905fe944f1cdbd2aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:a8c98e81a3b99149b2624638d761f73c50bb1f0fe8635af5c965bb367dfdc9e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b6be7185ef911caf0cff5b08b0061aba7e0e9c8d4d1718d4e89fa7e85d490`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:39:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:39:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 17:39:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 17:39:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:39:32 GMT
WORKDIR /root
# Tue, 14 Dec 2021 19:57:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba88e2b81c4f12b2ea6f779cb27400c7a946fd8234c4dcaccbd68daa7009b6`  
		Last Modified: Thu, 02 Dec 2021 17:42:16 GMT  
		Size: 44.4 MB (44399226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e35b1e2bc599c933280bb665519a8cc102dba7301afe868505bbaa5bc183d`  
		Last Modified: Thu, 02 Dec 2021 17:41:51 GMT  
		Size: 1.4 MB (1355908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e331f648f565998a32bd4ad9477c0990e10df0d5be4d5ce06a34a8ee00e779`  
		Last Modified: Tue, 14 Dec 2021 20:01:05 GMT  
		Size: 115.2 MB (115178100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
