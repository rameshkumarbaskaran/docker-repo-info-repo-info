<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.1`](#dart31)
-	[`dart:3.1-sdk`](#dart31-sdk)
-	[`dart:3.1.5`](#dart315)
-	[`dart:3.1.5-sdk`](#dart315-sdk)
-	[`dart:3.2.0-210.3.beta`](#dart320-2103beta)
-	[`dart:3.2.0-210.3.beta-sdk`](#dart320-2103beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:7274c299544918ebe2387652ac32bf80f76df8399cdce6125d3aca6411770657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:7abbc617e8b6e11c042e6a3a4ac3eb274582f8d69bb174a8fdbe6796520da56f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cb72fc911544d1e4c9c69ea67be3cd58714efa942fc80190394ba862e8d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 25 Oct 2023 18:19:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe941a9ca2cd99806d6214eb8721d82b2b81913a097c71d5eb6bc59bbfe89501`  
		Last Modified: Wed, 25 Oct 2023 18:20:32 GMT  
		Size: 210.6 MB (210554617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6e2b460961d416eb8235d89534290ad17f182cf0c0852240994bad8521a9adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294669374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb60377439ff668fbda55f387eb8d3d743f740beda25e8b8367f6742e2b68dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Wed, 25 Oct 2023 21:27:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56765750c91f183048d0f881facdddc9e55ed43f54980b1cd3de5379e11b52f8`  
		Last Modified: Wed, 25 Oct 2023 21:27:51 GMT  
		Size: 209.7 MB (209677666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3-sdk`

```console
$ docker pull dart@sha256:7274c299544918ebe2387652ac32bf80f76df8399cdce6125d3aca6411770657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7abbc617e8b6e11c042e6a3a4ac3eb274582f8d69bb174a8fdbe6796520da56f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cb72fc911544d1e4c9c69ea67be3cd58714efa942fc80190394ba862e8d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 25 Oct 2023 18:19:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe941a9ca2cd99806d6214eb8721d82b2b81913a097c71d5eb6bc59bbfe89501`  
		Last Modified: Wed, 25 Oct 2023 18:20:32 GMT  
		Size: 210.6 MB (210554617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6e2b460961d416eb8235d89534290ad17f182cf0c0852240994bad8521a9adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294669374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb60377439ff668fbda55f387eb8d3d743f740beda25e8b8367f6742e2b68dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Wed, 25 Oct 2023 21:27:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56765750c91f183048d0f881facdddc9e55ed43f54980b1cd3de5379e11b52f8`  
		Last Modified: Wed, 25 Oct 2023 21:27:51 GMT  
		Size: 209.7 MB (209677666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.1`

```console
$ docker pull dart@sha256:7274c299544918ebe2387652ac32bf80f76df8399cdce6125d3aca6411770657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1` - linux; amd64

```console
$ docker pull dart@sha256:7abbc617e8b6e11c042e6a3a4ac3eb274582f8d69bb174a8fdbe6796520da56f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cb72fc911544d1e4c9c69ea67be3cd58714efa942fc80190394ba862e8d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 25 Oct 2023 18:19:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe941a9ca2cd99806d6214eb8721d82b2b81913a097c71d5eb6bc59bbfe89501`  
		Last Modified: Wed, 25 Oct 2023 18:20:32 GMT  
		Size: 210.6 MB (210554617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6e2b460961d416eb8235d89534290ad17f182cf0c0852240994bad8521a9adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294669374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb60377439ff668fbda55f387eb8d3d743f740beda25e8b8367f6742e2b68dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Wed, 25 Oct 2023 21:27:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56765750c91f183048d0f881facdddc9e55ed43f54980b1cd3de5379e11b52f8`  
		Last Modified: Wed, 25 Oct 2023 21:27:51 GMT  
		Size: 209.7 MB (209677666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.1-sdk`

```console
$ docker pull dart@sha256:7274c299544918ebe2387652ac32bf80f76df8399cdce6125d3aca6411770657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7abbc617e8b6e11c042e6a3a4ac3eb274582f8d69bb174a8fdbe6796520da56f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cb72fc911544d1e4c9c69ea67be3cd58714efa942fc80190394ba862e8d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 25 Oct 2023 18:19:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe941a9ca2cd99806d6214eb8721d82b2b81913a097c71d5eb6bc59bbfe89501`  
		Last Modified: Wed, 25 Oct 2023 18:20:32 GMT  
		Size: 210.6 MB (210554617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6e2b460961d416eb8235d89534290ad17f182cf0c0852240994bad8521a9adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294669374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb60377439ff668fbda55f387eb8d3d743f740beda25e8b8367f6742e2b68dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Wed, 25 Oct 2023 21:27:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56765750c91f183048d0f881facdddc9e55ed43f54980b1cd3de5379e11b52f8`  
		Last Modified: Wed, 25 Oct 2023 21:27:51 GMT  
		Size: 209.7 MB (209677666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.1.5`

```console
$ docker pull dart@sha256:7274c299544918ebe2387652ac32bf80f76df8399cdce6125d3aca6411770657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1.5` - linux; amd64

```console
$ docker pull dart@sha256:7abbc617e8b6e11c042e6a3a4ac3eb274582f8d69bb174a8fdbe6796520da56f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cb72fc911544d1e4c9c69ea67be3cd58714efa942fc80190394ba862e8d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 25 Oct 2023 18:19:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe941a9ca2cd99806d6214eb8721d82b2b81913a097c71d5eb6bc59bbfe89501`  
		Last Modified: Wed, 25 Oct 2023 18:20:32 GMT  
		Size: 210.6 MB (210554617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1.5` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1.5` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6e2b460961d416eb8235d89534290ad17f182cf0c0852240994bad8521a9adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294669374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb60377439ff668fbda55f387eb8d3d743f740beda25e8b8367f6742e2b68dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Wed, 25 Oct 2023 21:27:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56765750c91f183048d0f881facdddc9e55ed43f54980b1cd3de5379e11b52f8`  
		Last Modified: Wed, 25 Oct 2023 21:27:51 GMT  
		Size: 209.7 MB (209677666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.1.5-sdk`

```console
$ docker pull dart@sha256:7274c299544918ebe2387652ac32bf80f76df8399cdce6125d3aca6411770657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1.5-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7abbc617e8b6e11c042e6a3a4ac3eb274582f8d69bb174a8fdbe6796520da56f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cb72fc911544d1e4c9c69ea67be3cd58714efa942fc80190394ba862e8d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 25 Oct 2023 18:19:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe941a9ca2cd99806d6214eb8721d82b2b81913a097c71d5eb6bc59bbfe89501`  
		Last Modified: Wed, 25 Oct 2023 18:20:32 GMT  
		Size: 210.6 MB (210554617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1.5-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1.5-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6e2b460961d416eb8235d89534290ad17f182cf0c0852240994bad8521a9adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294669374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb60377439ff668fbda55f387eb8d3d743f740beda25e8b8367f6742e2b68dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Wed, 25 Oct 2023 21:27:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56765750c91f183048d0f881facdddc9e55ed43f54980b1cd3de5379e11b52f8`  
		Last Modified: Wed, 25 Oct 2023 21:27:51 GMT  
		Size: 209.7 MB (209677666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.2.0-210.3.beta`

```console
$ docker pull dart@sha256:b817b708c1e8f93f186cf42e390ac4ba8de1b700d808947a6ce9c6c8c7c052c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2.0-210.3.beta` - linux; amd64

```console
$ docker pull dart@sha256:a1fedf327725f42891ed4fb295c466842fc53dab725cff2babacf7e7f7ae24df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db7ed24a511c0754178ac14253b73098625411c109fd8691881eb8a4d9fc138`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Thu, 19 Oct 2023 00:38:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c987877cc19cbd0aa4001b940a525dff824ef8878bab87684783da58c8496ab5`  
		Last Modified: Thu, 19 Oct 2023 00:40:35 GMT  
		Size: 223.0 MB (222976393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.3.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:cffc926c8b7a8069db406c1b876197a2723bc2e69572f25cdbed28be5204e9a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203524137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe82f05fcdfb5d74dbcfcdc549b51b459f3412ce75cce3756fedf450ef11719`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8955146e00195258dd3dbcfb37e8ff0652274da09b50decae8d29445a501346`  
		Last Modified: Wed, 01 Nov 2023 01:25:42 GMT  
		Size: 128.4 MB (128351099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.3.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c9ef4e296d2292b396fef7c1cd988672157ebc84864e2ac9e5f0564f7667189d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307154643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e56877ddb1201838c5e15bb54ca396a3432cf186f1775951ef8a8e13bf6ec8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Thu, 19 Oct 2023 01:25:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cee90ac8206c9cc8c5dcab46dc5ed954fa47b0d2b3dec794ea21d22d95e62d`  
		Last Modified: Thu, 19 Oct 2023 01:26:57 GMT  
		Size: 222.2 MB (222162935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.2.0-210.3.beta-sdk`

```console
$ docker pull dart@sha256:b817b708c1e8f93f186cf42e390ac4ba8de1b700d808947a6ce9c6c8c7c052c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2.0-210.3.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a1fedf327725f42891ed4fb295c466842fc53dab725cff2babacf7e7f7ae24df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db7ed24a511c0754178ac14253b73098625411c109fd8691881eb8a4d9fc138`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Thu, 19 Oct 2023 00:38:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c987877cc19cbd0aa4001b940a525dff824ef8878bab87684783da58c8496ab5`  
		Last Modified: Thu, 19 Oct 2023 00:40:35 GMT  
		Size: 223.0 MB (222976393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.3.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:cffc926c8b7a8069db406c1b876197a2723bc2e69572f25cdbed28be5204e9a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203524137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe82f05fcdfb5d74dbcfcdc549b51b459f3412ce75cce3756fedf450ef11719`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8955146e00195258dd3dbcfb37e8ff0652274da09b50decae8d29445a501346`  
		Last Modified: Wed, 01 Nov 2023 01:25:42 GMT  
		Size: 128.4 MB (128351099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.3.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c9ef4e296d2292b396fef7c1cd988672157ebc84864e2ac9e5f0564f7667189d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307154643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e56877ddb1201838c5e15bb54ca396a3432cf186f1775951ef8a8e13bf6ec8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Thu, 19 Oct 2023 01:25:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cee90ac8206c9cc8c5dcab46dc5ed954fa47b0d2b3dec794ea21d22d95e62d`  
		Last Modified: Thu, 19 Oct 2023 01:26:57 GMT  
		Size: 222.2 MB (222162935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:b817b708c1e8f93f186cf42e390ac4ba8de1b700d808947a6ce9c6c8c7c052c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:a1fedf327725f42891ed4fb295c466842fc53dab725cff2babacf7e7f7ae24df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db7ed24a511c0754178ac14253b73098625411c109fd8691881eb8a4d9fc138`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Thu, 19 Oct 2023 00:38:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c987877cc19cbd0aa4001b940a525dff824ef8878bab87684783da58c8496ab5`  
		Last Modified: Thu, 19 Oct 2023 00:40:35 GMT  
		Size: 223.0 MB (222976393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:cffc926c8b7a8069db406c1b876197a2723bc2e69572f25cdbed28be5204e9a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203524137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe82f05fcdfb5d74dbcfcdc549b51b459f3412ce75cce3756fedf450ef11719`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8955146e00195258dd3dbcfb37e8ff0652274da09b50decae8d29445a501346`  
		Last Modified: Wed, 01 Nov 2023 01:25:42 GMT  
		Size: 128.4 MB (128351099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c9ef4e296d2292b396fef7c1cd988672157ebc84864e2ac9e5f0564f7667189d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307154643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e56877ddb1201838c5e15bb54ca396a3432cf186f1775951ef8a8e13bf6ec8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Thu, 19 Oct 2023 01:25:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cee90ac8206c9cc8c5dcab46dc5ed954fa47b0d2b3dec794ea21d22d95e62d`  
		Last Modified: Thu, 19 Oct 2023 01:26:57 GMT  
		Size: 222.2 MB (222162935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:b817b708c1e8f93f186cf42e390ac4ba8de1b700d808947a6ce9c6c8c7c052c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a1fedf327725f42891ed4fb295c466842fc53dab725cff2babacf7e7f7ae24df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db7ed24a511c0754178ac14253b73098625411c109fd8691881eb8a4d9fc138`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Thu, 19 Oct 2023 00:38:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c987877cc19cbd0aa4001b940a525dff824ef8878bab87684783da58c8496ab5`  
		Last Modified: Thu, 19 Oct 2023 00:40:35 GMT  
		Size: 223.0 MB (222976393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:cffc926c8b7a8069db406c1b876197a2723bc2e69572f25cdbed28be5204e9a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203524137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe82f05fcdfb5d74dbcfcdc549b51b459f3412ce75cce3756fedf450ef11719`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8955146e00195258dd3dbcfb37e8ff0652274da09b50decae8d29445a501346`  
		Last Modified: Wed, 01 Nov 2023 01:25:42 GMT  
		Size: 128.4 MB (128351099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c9ef4e296d2292b396fef7c1cd988672157ebc84864e2ac9e5f0564f7667189d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307154643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e56877ddb1201838c5e15bb54ca396a3432cf186f1775951ef8a8e13bf6ec8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Thu, 19 Oct 2023 01:25:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b3aa85b15bd13d619ba924524d5c7f082dc256a062ad34fe12ec824c9f05c2b3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=08ec044e8b77a46d89073b5e312848b8f65b00f93a62aecd902613cef0ad1f9d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b7644435c8acf1e73da3f1ce16889b7222fbab37a75111aff225422a1cc61cab;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cee90ac8206c9cc8c5dcab46dc5ed954fa47b0d2b3dec794ea21d22d95e62d`  
		Last Modified: Thu, 19 Oct 2023 01:26:57 GMT  
		Size: 222.2 MB (222162935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:7274c299544918ebe2387652ac32bf80f76df8399cdce6125d3aca6411770657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:7abbc617e8b6e11c042e6a3a4ac3eb274582f8d69bb174a8fdbe6796520da56f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cb72fc911544d1e4c9c69ea67be3cd58714efa942fc80190394ba862e8d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 25 Oct 2023 18:19:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe941a9ca2cd99806d6214eb8721d82b2b81913a097c71d5eb6bc59bbfe89501`  
		Last Modified: Wed, 25 Oct 2023 18:20:32 GMT  
		Size: 210.6 MB (210554617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6e2b460961d416eb8235d89534290ad17f182cf0c0852240994bad8521a9adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294669374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb60377439ff668fbda55f387eb8d3d743f740beda25e8b8367f6742e2b68dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Wed, 25 Oct 2023 21:27:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56765750c91f183048d0f881facdddc9e55ed43f54980b1cd3de5379e11b52f8`  
		Last Modified: Wed, 25 Oct 2023 21:27:51 GMT  
		Size: 209.7 MB (209677666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:7274c299544918ebe2387652ac32bf80f76df8399cdce6125d3aca6411770657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:7abbc617e8b6e11c042e6a3a4ac3eb274582f8d69bb174a8fdbe6796520da56f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cb72fc911544d1e4c9c69ea67be3cd58714efa942fc80190394ba862e8d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 25 Oct 2023 18:19:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe941a9ca2cd99806d6214eb8721d82b2b81913a097c71d5eb6bc59bbfe89501`  
		Last Modified: Wed, 25 Oct 2023 18:20:32 GMT  
		Size: 210.6 MB (210554617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6e2b460961d416eb8235d89534290ad17f182cf0c0852240994bad8521a9adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294669374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb60377439ff668fbda55f387eb8d3d743f740beda25e8b8367f6742e2b68dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Wed, 25 Oct 2023 21:27:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56765750c91f183048d0f881facdddc9e55ed43f54980b1cd3de5379e11b52f8`  
		Last Modified: Wed, 25 Oct 2023 21:27:51 GMT  
		Size: 209.7 MB (209677666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:7274c299544918ebe2387652ac32bf80f76df8399cdce6125d3aca6411770657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:7abbc617e8b6e11c042e6a3a4ac3eb274582f8d69bb174a8fdbe6796520da56f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cb72fc911544d1e4c9c69ea67be3cd58714efa942fc80190394ba862e8d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 25 Oct 2023 18:19:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe941a9ca2cd99806d6214eb8721d82b2b81913a097c71d5eb6bc59bbfe89501`  
		Last Modified: Wed, 25 Oct 2023 18:20:32 GMT  
		Size: 210.6 MB (210554617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6e2b460961d416eb8235d89534290ad17f182cf0c0852240994bad8521a9adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294669374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb60377439ff668fbda55f387eb8d3d743f740beda25e8b8367f6742e2b68dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Wed, 25 Oct 2023 21:27:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56765750c91f183048d0f881facdddc9e55ed43f54980b1cd3de5379e11b52f8`  
		Last Modified: Wed, 25 Oct 2023 21:27:51 GMT  
		Size: 209.7 MB (209677666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:7274c299544918ebe2387652ac32bf80f76df8399cdce6125d3aca6411770657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7abbc617e8b6e11c042e6a3a4ac3eb274582f8d69bb174a8fdbe6796520da56f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cb72fc911544d1e4c9c69ea67be3cd58714efa942fc80190394ba862e8d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 25 Oct 2023 18:19:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe941a9ca2cd99806d6214eb8721d82b2b81913a097c71d5eb6bc59bbfe89501`  
		Last Modified: Wed, 25 Oct 2023 18:20:32 GMT  
		Size: 210.6 MB (210554617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d6e2b460961d416eb8235d89534290ad17f182cf0c0852240994bad8521a9adc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294669374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb60377439ff668fbda55f387eb8d3d743f740beda25e8b8367f6742e2b68dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:17:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:17:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 12 Oct 2023 10:17:40 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 12 Oct 2023 10:17:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 10:17:40 GMT
WORKDIR /root
# Wed, 25 Oct 2023 21:27:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7edca539e4b60c13376b1f5419e9fa3efb2541d698345e3ee79bc0dcb6e374`  
		Last Modified: Thu, 12 Oct 2023 10:18:27 GMT  
		Size: 54.3 MB (54318879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a1c0a25c7682a3b440ea832050e935d14e0586689fdae3f67be067e1ffe86`  
		Last Modified: Thu, 12 Oct 2023 10:18:21 GMT  
		Size: 1.5 MB (1493545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56765750c91f183048d0f881facdddc9e55ed43f54980b1cd3de5379e11b52f8`  
		Last Modified: Wed, 25 Oct 2023 21:27:51 GMT  
		Size: 209.7 MB (209677666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
