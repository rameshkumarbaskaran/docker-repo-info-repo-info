## `dart:beta`

```console
$ docker pull dart@sha256:d9c7c47097e8149a4de743e2c224a143283b2d757041be249ff0457fe80b7157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:5fb698c392035ce722ac81fb5009ababeb5bb938cdbb3f6a28eb23cbe9d8b26d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (303020110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118c228dbc71ba4684e54a4a9496262d50f00e1db0085f0fda03935be9698788`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 07:21:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 07:21:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 16 Aug 2023 07:21:32 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 18 Aug 2023 23:19:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Aug 2023 23:19:26 GMT
WORKDIR /root
# Fri, 01 Sep 2023 19:23:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bd0311f604def7e49215c6fbed823dc01284586f83963b6891cc6dee36da2488;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8bb319c661278852b371bd4438cc6e19860d0613bfe3d016006bd6ef6bf9e72f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=02de2c59d14fe4fcbcc6da756457be6966cd399bee507b2980d0e3c76fa4a2e3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-42.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2577ff5100d24131ef5c0b1d5abb88623898588a87bafbed311deab71d09ee`  
		Last Modified: Wed, 16 Aug 2023 07:22:28 GMT  
		Size: 45.1 MB (45101830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4d59ba3d1a7503ca685749da21497c47644df01b1409c1ce14a6d494fd9436`  
		Last Modified: Wed, 16 Aug 2023 07:22:22 GMT  
		Size: 2.2 MB (2160697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ac73fe6ce0b7ec108bfbb51e8f032f3eb90b016f93022f1bfb19dc02857872`  
		Last Modified: Fri, 01 Sep 2023 19:23:49 GMT  
		Size: 224.3 MB (224339905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:de584e18186a3f76a3868a16bb3f2bad8aed4b995e62d076b01cf32b8704c674
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185617293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c6cb99e75ef88df74a7bc77a9f49f55ab2d1d387f61dc1749f9e7a5659e78a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:17:33 GMT
ADD file:d9383f6a4370dbf4af8e05edac181465a410899022cf1788f9001a976b9beecd in / 
# Wed, 16 Aug 2023 00:17:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:00:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:00:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 16 Aug 2023 15:00:35 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 18 Aug 2023 23:57:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Aug 2023 23:57:18 GMT
WORKDIR /root
# Fri, 01 Sep 2023 20:01:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bd0311f604def7e49215c6fbed823dc01284586f83963b6891cc6dee36da2488;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8bb319c661278852b371bd4438cc6e19860d0613bfe3d016006bd6ef6bf9e72f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=02de2c59d14fe4fcbcc6da756457be6966cd399bee507b2980d0e3c76fa4a2e3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-42.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66971a88ba9c0b0ac6503475f1bc4981010269bdba2638318b63c625ee44cd79`  
		Last Modified: Wed, 16 Aug 2023 00:22:09 GMT  
		Size: 26.6 MB (26578637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9550e27958af98a4d93dc3dbcd1edcfafd99d14de8df8b555d57510383ce97a`  
		Last Modified: Wed, 16 Aug 2023 15:01:37 GMT  
		Size: 41.0 MB (40988435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555b973d8367ff0c896fa7540e845348f6d8f5dd0136861e82f831ccf4384b81`  
		Last Modified: Wed, 16 Aug 2023 15:01:28 GMT  
		Size: 1.3 MB (1287722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa84aff55951d342edc4ee77e2264ee67bd919ce359679e558604d6b527f311`  
		Last Modified: Fri, 01 Sep 2023 20:02:11 GMT  
		Size: 116.8 MB (116762499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ea5b7d54d41eea1f1b17354217c4f1303882487ac1296520ca431a9e601cf6c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f859467c244af46671e9484df9da3c9577b42cb97c7138f7c20377d225f79c1e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:02:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:02:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 16 Aug 2023 02:02:18 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 18 Aug 2023 23:39:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Aug 2023 23:39:25 GMT
WORKDIR /root
# Fri, 01 Sep 2023 19:40:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bd0311f604def7e49215c6fbed823dc01284586f83963b6891cc6dee36da2488;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8bb319c661278852b371bd4438cc6e19860d0613bfe3d016006bd6ef6bf9e72f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=02de2c59d14fe4fcbcc6da756457be6966cd399bee507b2980d0e3c76fa4a2e3;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-42.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c88ee4e2ded4b674611c7a0cc207fa18d0c207f6898b4c4a97598b60dc687d3`  
		Last Modified: Wed, 16 Aug 2023 02:03:00 GMT  
		Size: 45.0 MB (45011889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26f4393bc25a5d3316c200e692678aa19db82688e7b1d5442111eecc8273919`  
		Last Modified: Wed, 16 Aug 2023 02:02:55 GMT  
		Size: 1.6 MB (1560880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca2d1b7c7931a0f8b124e71f2500ff4fc00fc41b3e8c47f5b80e1b813b29d30`  
		Last Modified: Fri, 01 Sep 2023 19:40:54 GMT  
		Size: 118.2 MB (118154050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
