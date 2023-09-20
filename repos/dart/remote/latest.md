## `dart:latest`

```console
$ docker pull dart@sha256:33de30a1e17e42ce37992fdf50d33e78cda9d601b63b474146e8ef987cde7941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:a154d77a8df7aeac46fdf15edd72f01c03b1b569e1a4c80263c22e1245507d21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291212052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a153eb9f6233ac99da9c56f5f918af34424e56193054b0735e3864b707e69910`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:18:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:18:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 20 Sep 2023 07:18:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Sep 2023 07:18:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:18:45 GMT
WORKDIR /root
# Wed, 20 Sep 2023 07:18:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=be679ccef3a0b28f19e296dd5b6374ac60dd0deb06d4d663da9905190489d48b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0be45ee5992be715cf57970f8b37f5be26d3be30202c420ce1606e10147223f0;             SDK_ARCH="arm";;         arm64)             DART_SHA256=395180693ccc758e4e830d3b13c4879e6e96b6869763a56e91721bf9d4228250;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bf0a41b9b2ddc3d0dd483a225310d910dd75e6b06cb471ce58ea2f00746c70`  
		Last Modified: Wed, 20 Sep 2023 07:19:44 GMT  
		Size: 45.1 MB (45101748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c5dc469f81d51f216c049afa60b6dd06c8bde86511e756dd7a9fb3770bc65`  
		Last Modified: Wed, 20 Sep 2023 07:19:38 GMT  
		Size: 2.2 MB (2160693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b206b8292a2bd320d4057f1b0e671d6114d33e7ab197acc9977b9bce38a101f`  
		Last Modified: Wed, 20 Sep 2023 07:20:06 GMT  
		Size: 212.5 MB (212531900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f86372e8e91d4dadc210b72bd08c7fc3f8cc9afe694df5b42a57a912943ca5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.2 MB (182227517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717a055aee6de28bdaceb277a6b5efe5e06d2ceed9bcaa3e9e36f9b7e5a8de6a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:58:09 GMT
ADD file:d714939aacc810de397a02461ce4b9dd85e92783aff066bd3da685e3d2d97439 in / 
# Thu, 07 Sep 2023 00:58:10 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:55:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:55:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 07 Sep 2023 01:55:59 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 07 Sep 2023 01:55:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 01:55:59 GMT
WORKDIR /root
# Wed, 13 Sep 2023 21:57:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=be679ccef3a0b28f19e296dd5b6374ac60dd0deb06d4d663da9905190489d48b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0be45ee5992be715cf57970f8b37f5be26d3be30202c420ce1606e10147223f0;             SDK_ARCH="arm";;         arm64)             DART_SHA256=395180693ccc758e4e830d3b13c4879e6e96b6869763a56e91721bf9d4228250;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:323242406c24248128abc25e113055d272350b4ac4ecd985dbabfb7061c48d49`  
		Last Modified: Thu, 07 Sep 2023 01:03:12 GMT  
		Size: 26.6 MB (26578710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeaeabc9eed5e4b6207b4f729dc6c8f8acc154299578e082a7e1e6d570a18b6`  
		Last Modified: Thu, 07 Sep 2023 01:56:59 GMT  
		Size: 41.0 MB (40988287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf7fe56ae6697aba2588a366d664e58dc3243c87d2f1ac39d7b64fe1a6a7914`  
		Last Modified: Thu, 07 Sep 2023 01:56:49 GMT  
		Size: 1.3 MB (1287721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a510e002775c32dd74af3337ec4f90c7460ed4caf0fc52dfcbc9d46ab2384a88`  
		Last Modified: Wed, 13 Sep 2023 21:58:04 GMT  
		Size: 113.4 MB (113372799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eb845d64cd21b579ad615166533b957dd715aedeaea4b5e49465cac22509b19c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191389445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6118dd01519fc4ad170ab02874e9e58008a135870fd9910bbfbe29cdc199890`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:41:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:41:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 20 Sep 2023 09:41:40 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Sep 2023 09:41:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 09:41:40 GMT
WORKDIR /root
# Wed, 20 Sep 2023 09:41:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=be679ccef3a0b28f19e296dd5b6374ac60dd0deb06d4d663da9905190489d48b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0be45ee5992be715cf57970f8b37f5be26d3be30202c420ce1606e10147223f0;             SDK_ARCH="arm";;         arm64)             DART_SHA256=395180693ccc758e4e830d3b13c4879e6e96b6869763a56e91721bf9d4228250;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac824db015ccf6a2dbf9dce2697d458627637e808fe71dfef1cdfa299a8ed33`  
		Last Modified: Wed, 20 Sep 2023 09:42:26 GMT  
		Size: 45.0 MB (45011925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d638d44b97aa7b99ac9b8c06bc5658abf32a34a5d7ae33a7893364fa64173`  
		Last Modified: Wed, 20 Sep 2023 09:42:21 GMT  
		Size: 1.6 MB (1560884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f7b621f2b0bb7a1e8488403686f419f1910d73727ad838a63046ea0cdc1516`  
		Last Modified: Wed, 20 Sep 2023 09:42:33 GMT  
		Size: 114.8 MB (114753767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
