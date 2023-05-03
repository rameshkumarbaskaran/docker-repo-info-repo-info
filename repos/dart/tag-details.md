<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:2`](#dart2)
-	[`dart:2-sdk`](#dart2-sdk)
-	[`dart:2.19`](#dart219)
-	[`dart:2.19-sdk`](#dart219-sdk)
-	[`dart:2.19.6`](#dart2196)
-	[`dart:2.19.6-sdk`](#dart2196-sdk)
-	[`dart:3.0.0-417.4.beta`](#dart300-4174beta)
-	[`dart:3.0.0-417.4.beta-sdk`](#dart300-4174beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:2`

```console
$ docker pull dart@sha256:4b746768b82e2f650bb4b0bbec19f5da60d9649adb8d93d65f722028689f76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2` - linux; amd64

```console
$ docker pull dart@sha256:3ee2c8367ea715fbfeefbec63f43dee38b8978bfac957dbafda65573fef2d201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300594019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca770f54f62574c05e94895a1e3f0f7b2e77624b8c8cd78bcd1897fbfcf6ad93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:47:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714a23c50c6595f5ec143279e97d66ed398dcfc948830eeebf0b5aa6ac57176`  
		Last Modified: Wed, 03 May 2023 20:49:03 GMT  
		Size: 221.9 MB (221927080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm variant v7

```console
$ docker pull dart@sha256:e490df0aa8779794b953cd5309b79fb48c4a3eae38d6b8a909ed21a82353eea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196744669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db76263e25d7e72cd0ed854226eef20548ad5fda81167ab582b0cc76a576d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdce362b867fbacb8e818a841da8cfc7c19fdf5070e236d6433c80a72cc6408`  
		Last Modified: Wed, 03 May 2023 22:31:00 GMT  
		Size: 127.9 MB (127903864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70740db9149f0456e07c23852ae990dbf21ab9f34cab65126ef67c5a10becfc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe885d6a8170f1ce8f45dcb811539c2d0220ee9900a72b833264c5ae78b0f9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:01:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360e393242fd8893b744aea8fe841b075de8e50467c1a8f590342451e8a886b`  
		Last Modified: Wed, 03 May 2023 18:02:36 GMT  
		Size: 129.4 MB (129352757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2-sdk`

```console
$ docker pull dart@sha256:4b746768b82e2f650bb4b0bbec19f5da60d9649adb8d93d65f722028689f76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:3ee2c8367ea715fbfeefbec63f43dee38b8978bfac957dbafda65573fef2d201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300594019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca770f54f62574c05e94895a1e3f0f7b2e77624b8c8cd78bcd1897fbfcf6ad93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:47:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714a23c50c6595f5ec143279e97d66ed398dcfc948830eeebf0b5aa6ac57176`  
		Last Modified: Wed, 03 May 2023 20:49:03 GMT  
		Size: 221.9 MB (221927080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e490df0aa8779794b953cd5309b79fb48c4a3eae38d6b8a909ed21a82353eea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196744669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db76263e25d7e72cd0ed854226eef20548ad5fda81167ab582b0cc76a576d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdce362b867fbacb8e818a841da8cfc7c19fdf5070e236d6433c80a72cc6408`  
		Last Modified: Wed, 03 May 2023 22:31:00 GMT  
		Size: 127.9 MB (127903864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70740db9149f0456e07c23852ae990dbf21ab9f34cab65126ef67c5a10becfc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe885d6a8170f1ce8f45dcb811539c2d0220ee9900a72b833264c5ae78b0f9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:01:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360e393242fd8893b744aea8fe841b075de8e50467c1a8f590342451e8a886b`  
		Last Modified: Wed, 03 May 2023 18:02:36 GMT  
		Size: 129.4 MB (129352757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19`

```console
$ docker pull dart@sha256:4b746768b82e2f650bb4b0bbec19f5da60d9649adb8d93d65f722028689f76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19` - linux; amd64

```console
$ docker pull dart@sha256:3ee2c8367ea715fbfeefbec63f43dee38b8978bfac957dbafda65573fef2d201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300594019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca770f54f62574c05e94895a1e3f0f7b2e77624b8c8cd78bcd1897fbfcf6ad93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:47:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714a23c50c6595f5ec143279e97d66ed398dcfc948830eeebf0b5aa6ac57176`  
		Last Modified: Wed, 03 May 2023 20:49:03 GMT  
		Size: 221.9 MB (221927080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19` - linux; arm variant v7

```console
$ docker pull dart@sha256:e490df0aa8779794b953cd5309b79fb48c4a3eae38d6b8a909ed21a82353eea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196744669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db76263e25d7e72cd0ed854226eef20548ad5fda81167ab582b0cc76a576d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdce362b867fbacb8e818a841da8cfc7c19fdf5070e236d6433c80a72cc6408`  
		Last Modified: Wed, 03 May 2023 22:31:00 GMT  
		Size: 127.9 MB (127903864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70740db9149f0456e07c23852ae990dbf21ab9f34cab65126ef67c5a10becfc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe885d6a8170f1ce8f45dcb811539c2d0220ee9900a72b833264c5ae78b0f9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:01:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360e393242fd8893b744aea8fe841b075de8e50467c1a8f590342451e8a886b`  
		Last Modified: Wed, 03 May 2023 18:02:36 GMT  
		Size: 129.4 MB (129352757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19-sdk`

```console
$ docker pull dart@sha256:4b746768b82e2f650bb4b0bbec19f5da60d9649adb8d93d65f722028689f76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19-sdk` - linux; amd64

```console
$ docker pull dart@sha256:3ee2c8367ea715fbfeefbec63f43dee38b8978bfac957dbafda65573fef2d201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300594019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca770f54f62574c05e94895a1e3f0f7b2e77624b8c8cd78bcd1897fbfcf6ad93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:47:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714a23c50c6595f5ec143279e97d66ed398dcfc948830eeebf0b5aa6ac57176`  
		Last Modified: Wed, 03 May 2023 20:49:03 GMT  
		Size: 221.9 MB (221927080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e490df0aa8779794b953cd5309b79fb48c4a3eae38d6b8a909ed21a82353eea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196744669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db76263e25d7e72cd0ed854226eef20548ad5fda81167ab582b0cc76a576d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdce362b867fbacb8e818a841da8cfc7c19fdf5070e236d6433c80a72cc6408`  
		Last Modified: Wed, 03 May 2023 22:31:00 GMT  
		Size: 127.9 MB (127903864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70740db9149f0456e07c23852ae990dbf21ab9f34cab65126ef67c5a10becfc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe885d6a8170f1ce8f45dcb811539c2d0220ee9900a72b833264c5ae78b0f9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:01:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360e393242fd8893b744aea8fe841b075de8e50467c1a8f590342451e8a886b`  
		Last Modified: Wed, 03 May 2023 18:02:36 GMT  
		Size: 129.4 MB (129352757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19.6`

```console
$ docker pull dart@sha256:4b746768b82e2f650bb4b0bbec19f5da60d9649adb8d93d65f722028689f76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19.6` - linux; amd64

```console
$ docker pull dart@sha256:3ee2c8367ea715fbfeefbec63f43dee38b8978bfac957dbafda65573fef2d201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300594019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca770f54f62574c05e94895a1e3f0f7b2e77624b8c8cd78bcd1897fbfcf6ad93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:47:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714a23c50c6595f5ec143279e97d66ed398dcfc948830eeebf0b5aa6ac57176`  
		Last Modified: Wed, 03 May 2023 20:49:03 GMT  
		Size: 221.9 MB (221927080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.6` - linux; arm variant v7

```console
$ docker pull dart@sha256:e490df0aa8779794b953cd5309b79fb48c4a3eae38d6b8a909ed21a82353eea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196744669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db76263e25d7e72cd0ed854226eef20548ad5fda81167ab582b0cc76a576d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdce362b867fbacb8e818a841da8cfc7c19fdf5070e236d6433c80a72cc6408`  
		Last Modified: Wed, 03 May 2023 22:31:00 GMT  
		Size: 127.9 MB (127903864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.6` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70740db9149f0456e07c23852ae990dbf21ab9f34cab65126ef67c5a10becfc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe885d6a8170f1ce8f45dcb811539c2d0220ee9900a72b833264c5ae78b0f9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:01:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360e393242fd8893b744aea8fe841b075de8e50467c1a8f590342451e8a886b`  
		Last Modified: Wed, 03 May 2023 18:02:36 GMT  
		Size: 129.4 MB (129352757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19.6-sdk`

```console
$ docker pull dart@sha256:4b746768b82e2f650bb4b0bbec19f5da60d9649adb8d93d65f722028689f76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19.6-sdk` - linux; amd64

```console
$ docker pull dart@sha256:3ee2c8367ea715fbfeefbec63f43dee38b8978bfac957dbafda65573fef2d201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300594019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca770f54f62574c05e94895a1e3f0f7b2e77624b8c8cd78bcd1897fbfcf6ad93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:47:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714a23c50c6595f5ec143279e97d66ed398dcfc948830eeebf0b5aa6ac57176`  
		Last Modified: Wed, 03 May 2023 20:49:03 GMT  
		Size: 221.9 MB (221927080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.6-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e490df0aa8779794b953cd5309b79fb48c4a3eae38d6b8a909ed21a82353eea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196744669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db76263e25d7e72cd0ed854226eef20548ad5fda81167ab582b0cc76a576d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdce362b867fbacb8e818a841da8cfc7c19fdf5070e236d6433c80a72cc6408`  
		Last Modified: Wed, 03 May 2023 22:31:00 GMT  
		Size: 127.9 MB (127903864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.6-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70740db9149f0456e07c23852ae990dbf21ab9f34cab65126ef67c5a10becfc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe885d6a8170f1ce8f45dcb811539c2d0220ee9900a72b833264c5ae78b0f9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:01:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360e393242fd8893b744aea8fe841b075de8e50467c1a8f590342451e8a886b`  
		Last Modified: Wed, 03 May 2023 18:02:36 GMT  
		Size: 129.4 MB (129352757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.0.0-417.4.beta`

```console
$ docker pull dart@sha256:81b5c0907f1d9d02c055ee2b58253e053deffc424426db6158fed9c424107be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.0.0-417.4.beta` - linux; amd64

```console
$ docker pull dart@sha256:0804678d928dff66c29c98525dc1faa60bd729fd4d726ce5ce308de7bc5d6f69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296531755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a3b322814e2d97cb3e1ae65d9044d51bdbc8b11711acb2834e4917fa47f0bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:48:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a9600ee40946d17a47e07dfa9b92fca765d0c64505a1ad06f347e609768a0b`  
		Last Modified: Wed, 03 May 2023 20:49:53 GMT  
		Size: 217.9 MB (217864816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.0.0-417.4.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:e5287687380be27b46bdfa78e7537768a85e47ec4e66810a40e6b00341b65d04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191250465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa15def3bea27bfab1c64e020b333c0590636bf2a31cea0c805f61083b1858c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6934e6c2bc216c8619ba267034128313469fc8bef2334e2ed6e084156b508b6e`  
		Last Modified: Wed, 03 May 2023 22:31:40 GMT  
		Size: 122.4 MB (122409660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.0.0-417.4.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5da1c5a956b0223cecb03d568f3a917325b7543e99c7c317c2819dd89d6208ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200419896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4355d56542c7e3ab4d7d2844fd2d835882fd249e803d2fd86bfd34cffbad669d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:02:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9385728308fc6ac286476846c3e7d368c03495f974e25cab972dfec52724f4e8`  
		Last Modified: Wed, 03 May 2023 18:03:11 GMT  
		Size: 123.8 MB (123795138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.0.0-417.4.beta-sdk`

```console
$ docker pull dart@sha256:81b5c0907f1d9d02c055ee2b58253e053deffc424426db6158fed9c424107be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.0.0-417.4.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:0804678d928dff66c29c98525dc1faa60bd729fd4d726ce5ce308de7bc5d6f69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296531755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a3b322814e2d97cb3e1ae65d9044d51bdbc8b11711acb2834e4917fa47f0bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:48:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a9600ee40946d17a47e07dfa9b92fca765d0c64505a1ad06f347e609768a0b`  
		Last Modified: Wed, 03 May 2023 20:49:53 GMT  
		Size: 217.9 MB (217864816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.0.0-417.4.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e5287687380be27b46bdfa78e7537768a85e47ec4e66810a40e6b00341b65d04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191250465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa15def3bea27bfab1c64e020b333c0590636bf2a31cea0c805f61083b1858c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6934e6c2bc216c8619ba267034128313469fc8bef2334e2ed6e084156b508b6e`  
		Last Modified: Wed, 03 May 2023 22:31:40 GMT  
		Size: 122.4 MB (122409660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.0.0-417.4.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5da1c5a956b0223cecb03d568f3a917325b7543e99c7c317c2819dd89d6208ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200419896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4355d56542c7e3ab4d7d2844fd2d835882fd249e803d2fd86bfd34cffbad669d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:02:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9385728308fc6ac286476846c3e7d368c03495f974e25cab972dfec52724f4e8`  
		Last Modified: Wed, 03 May 2023 18:03:11 GMT  
		Size: 123.8 MB (123795138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:81b5c0907f1d9d02c055ee2b58253e053deffc424426db6158fed9c424107be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:0804678d928dff66c29c98525dc1faa60bd729fd4d726ce5ce308de7bc5d6f69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296531755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a3b322814e2d97cb3e1ae65d9044d51bdbc8b11711acb2834e4917fa47f0bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:48:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a9600ee40946d17a47e07dfa9b92fca765d0c64505a1ad06f347e609768a0b`  
		Last Modified: Wed, 03 May 2023 20:49:53 GMT  
		Size: 217.9 MB (217864816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:e5287687380be27b46bdfa78e7537768a85e47ec4e66810a40e6b00341b65d04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191250465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa15def3bea27bfab1c64e020b333c0590636bf2a31cea0c805f61083b1858c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6934e6c2bc216c8619ba267034128313469fc8bef2334e2ed6e084156b508b6e`  
		Last Modified: Wed, 03 May 2023 22:31:40 GMT  
		Size: 122.4 MB (122409660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5da1c5a956b0223cecb03d568f3a917325b7543e99c7c317c2819dd89d6208ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200419896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4355d56542c7e3ab4d7d2844fd2d835882fd249e803d2fd86bfd34cffbad669d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:02:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9385728308fc6ac286476846c3e7d368c03495f974e25cab972dfec52724f4e8`  
		Last Modified: Wed, 03 May 2023 18:03:11 GMT  
		Size: 123.8 MB (123795138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:81b5c0907f1d9d02c055ee2b58253e053deffc424426db6158fed9c424107be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:0804678d928dff66c29c98525dc1faa60bd729fd4d726ce5ce308de7bc5d6f69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296531755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a3b322814e2d97cb3e1ae65d9044d51bdbc8b11711acb2834e4917fa47f0bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:48:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a9600ee40946d17a47e07dfa9b92fca765d0c64505a1ad06f347e609768a0b`  
		Last Modified: Wed, 03 May 2023 20:49:53 GMT  
		Size: 217.9 MB (217864816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e5287687380be27b46bdfa78e7537768a85e47ec4e66810a40e6b00341b65d04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191250465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa15def3bea27bfab1c64e020b333c0590636bf2a31cea0c805f61083b1858c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6934e6c2bc216c8619ba267034128313469fc8bef2334e2ed6e084156b508b6e`  
		Last Modified: Wed, 03 May 2023 22:31:40 GMT  
		Size: 122.4 MB (122409660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5da1c5a956b0223cecb03d568f3a917325b7543e99c7c317c2819dd89d6208ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200419896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4355d56542c7e3ab4d7d2844fd2d835882fd249e803d2fd86bfd34cffbad669d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:02:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d287ee249beb4a0cd869bc7d89c154a1fd444d4980e124eafc60241023a3bf4b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=89fec24ce5ea755e7929f756b85d423842bee8647f183c5473c3b6f8ceb9bc4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ae45811c30d500ae65e22606fc42e07bc2146d1ab42dc17a7fdbcbf940d82f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-417.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9385728308fc6ac286476846c3e7d368c03495f974e25cab972dfec52724f4e8`  
		Last Modified: Wed, 03 May 2023 18:03:11 GMT  
		Size: 123.8 MB (123795138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:4b746768b82e2f650bb4b0bbec19f5da60d9649adb8d93d65f722028689f76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:3ee2c8367ea715fbfeefbec63f43dee38b8978bfac957dbafda65573fef2d201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300594019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca770f54f62574c05e94895a1e3f0f7b2e77624b8c8cd78bcd1897fbfcf6ad93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:47:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714a23c50c6595f5ec143279e97d66ed398dcfc948830eeebf0b5aa6ac57176`  
		Last Modified: Wed, 03 May 2023 20:49:03 GMT  
		Size: 221.9 MB (221927080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:e490df0aa8779794b953cd5309b79fb48c4a3eae38d6b8a909ed21a82353eea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196744669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db76263e25d7e72cd0ed854226eef20548ad5fda81167ab582b0cc76a576d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdce362b867fbacb8e818a841da8cfc7c19fdf5070e236d6433c80a72cc6408`  
		Last Modified: Wed, 03 May 2023 22:31:00 GMT  
		Size: 127.9 MB (127903864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70740db9149f0456e07c23852ae990dbf21ab9f34cab65126ef67c5a10becfc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe885d6a8170f1ce8f45dcb811539c2d0220ee9900a72b833264c5ae78b0f9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:01:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360e393242fd8893b744aea8fe841b075de8e50467c1a8f590342451e8a886b`  
		Last Modified: Wed, 03 May 2023 18:02:36 GMT  
		Size: 129.4 MB (129352757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:4b746768b82e2f650bb4b0bbec19f5da60d9649adb8d93d65f722028689f76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:3ee2c8367ea715fbfeefbec63f43dee38b8978bfac957dbafda65573fef2d201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300594019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca770f54f62574c05e94895a1e3f0f7b2e77624b8c8cd78bcd1897fbfcf6ad93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:47:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714a23c50c6595f5ec143279e97d66ed398dcfc948830eeebf0b5aa6ac57176`  
		Last Modified: Wed, 03 May 2023 20:49:03 GMT  
		Size: 221.9 MB (221927080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e490df0aa8779794b953cd5309b79fb48c4a3eae38d6b8a909ed21a82353eea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196744669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db76263e25d7e72cd0ed854226eef20548ad5fda81167ab582b0cc76a576d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdce362b867fbacb8e818a841da8cfc7c19fdf5070e236d6433c80a72cc6408`  
		Last Modified: Wed, 03 May 2023 22:31:00 GMT  
		Size: 127.9 MB (127903864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70740db9149f0456e07c23852ae990dbf21ab9f34cab65126ef67c5a10becfc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe885d6a8170f1ce8f45dcb811539c2d0220ee9900a72b833264c5ae78b0f9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:01:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360e393242fd8893b744aea8fe841b075de8e50467c1a8f590342451e8a886b`  
		Last Modified: Wed, 03 May 2023 18:02:36 GMT  
		Size: 129.4 MB (129352757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:4b746768b82e2f650bb4b0bbec19f5da60d9649adb8d93d65f722028689f76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:3ee2c8367ea715fbfeefbec63f43dee38b8978bfac957dbafda65573fef2d201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300594019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca770f54f62574c05e94895a1e3f0f7b2e77624b8c8cd78bcd1897fbfcf6ad93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:47:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714a23c50c6595f5ec143279e97d66ed398dcfc948830eeebf0b5aa6ac57176`  
		Last Modified: Wed, 03 May 2023 20:49:03 GMT  
		Size: 221.9 MB (221927080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:e490df0aa8779794b953cd5309b79fb48c4a3eae38d6b8a909ed21a82353eea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196744669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db76263e25d7e72cd0ed854226eef20548ad5fda81167ab582b0cc76a576d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdce362b867fbacb8e818a841da8cfc7c19fdf5070e236d6433c80a72cc6408`  
		Last Modified: Wed, 03 May 2023 22:31:00 GMT  
		Size: 127.9 MB (127903864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70740db9149f0456e07c23852ae990dbf21ab9f34cab65126ef67c5a10becfc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe885d6a8170f1ce8f45dcb811539c2d0220ee9900a72b833264c5ae78b0f9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:01:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360e393242fd8893b744aea8fe841b075de8e50467c1a8f590342451e8a886b`  
		Last Modified: Wed, 03 May 2023 18:02:36 GMT  
		Size: 129.4 MB (129352757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:4b746768b82e2f650bb4b0bbec19f5da60d9649adb8d93d65f722028689f76c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:3ee2c8367ea715fbfeefbec63f43dee38b8978bfac957dbafda65573fef2d201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300594019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca770f54f62574c05e94895a1e3f0f7b2e77624b8c8cd78bcd1897fbfcf6ad93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:47:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 20:47:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 20:47:45 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:47:45 GMT
WORKDIR /root
# Wed, 03 May 2023 20:47:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595f13a7ddbfbf5f060d3134f266de9375b4b50f9c6235f694b4d6ab0173cf5`  
		Last Modified: Wed, 03 May 2023 20:48:40 GMT  
		Size: 45.1 MB (45102730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48dfc94881b3cd15638ea2057d880046b465e441a83c8bec205a5076860df72`  
		Last Modified: Wed, 03 May 2023 20:48:34 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714a23c50c6595f5ec143279e97d66ed398dcfc948830eeebf0b5aa6ac57176`  
		Last Modified: Wed, 03 May 2023 20:49:03 GMT  
		Size: 221.9 MB (221927080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e490df0aa8779794b953cd5309b79fb48c4a3eae38d6b8a909ed21a82353eea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196744669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3db76263e25d7e72cd0ed854226eef20548ad5fda81167ab582b0cc76a576d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:29:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:29:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 22:29:54 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 22:29:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 22:29:54 GMT
WORKDIR /root
# Wed, 03 May 2023 22:30:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7d9f1dfe5dc181109336980c47015c432d0cd04330b71377a5e9cdbe3944c8`  
		Last Modified: Wed, 03 May 2023 22:30:44 GMT  
		Size: 41.0 MB (40988433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e3b3ad8ad92505ee3309dd2dcc5b16662c5cb604d58a1584970fbab09bb526`  
		Last Modified: Wed, 03 May 2023 22:30:38 GMT  
		Size: 1.3 MB (1287724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdce362b867fbacb8e818a841da8cfc7c19fdf5070e236d6433c80a72cc6408`  
		Last Modified: Wed, 03 May 2023 22:31:00 GMT  
		Size: 127.9 MB (127903864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70740db9149f0456e07c23852ae990dbf21ab9f34cab65126ef67c5a10becfc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe885d6a8170f1ce8f45dcb811539c2d0220ee9900a72b833264c5ae78b0f9a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 03 May 2023 18:01:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 03 May 2023 18:01:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:44 GMT
WORKDIR /root
# Wed, 03 May 2023 18:01:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0fdff25e6acba3d6094155a7e341634f8de3477e86c2fda4ad47232c1adf704f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7286b3a935c98ec9731c6e540614ef20e8ad8a1d6bef194c79e29d9837363de3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=6913b7c0b3b78bc141d372cd473da21771e57372b1ab45c977ce1550c8ff0b9c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc0b14711e98b08b1a032b2deb48049f18fd73081b8c279a065a4c3d917122`  
		Last Modified: Wed, 03 May 2023 18:02:26 GMT  
		Size: 45.0 MB (45011139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e1fa58a15ccb7cc2d05484fac11f66090b0c7d8833a0193a8c9c036c8e171`  
		Last Modified: Wed, 03 May 2023 18:02:22 GMT  
		Size: 1.6 MB (1560886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4360e393242fd8893b744aea8fe841b075de8e50467c1a8f590342451e8a886b`  
		Last Modified: Wed, 03 May 2023 18:02:36 GMT  
		Size: 129.4 MB (129352757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
