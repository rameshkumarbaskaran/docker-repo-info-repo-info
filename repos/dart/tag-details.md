<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:2`](#dart2)
-	[`dart:2-sdk`](#dart2-sdk)
-	[`dart:2.18`](#dart218)
-	[`dart:2.18-sdk`](#dart218-sdk)
-	[`dart:2.18.6`](#dart2186)
-	[`dart:2.18.6-sdk`](#dart2186-sdk)
-	[`dart:2.19.0-444.2.beta`](#dart2190-4442beta)
-	[`dart:2.19.0-444.2.beta-sdk`](#dart2190-4442beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:2`

```console
$ docker pull dart@sha256:2f5be872ec113b108545b05b5d5e6f07ff01eee0cb3d2514d0492d546395b254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2` - linux; amd64

```console
$ docker pull dart@sha256:7ce70683367f221ea23434d69cdc42ee3f533592f496b5e33f559f7f9014c6ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271946081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcadef020af0bf7e217b539e2e1d22506c5c3977f50558106563c1afdbab4c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0b40a320683da865803676e13fef8e4bdd8ba35925bee685b9249e15365a9`  
		Last Modified: Sat, 17 Dec 2022 02:48:31 GMT  
		Size: 193.3 MB (193296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3ec8df88cc0f722d53ac4ed18cd6a3fb0a49b169dac51dd45f8985f3176a2132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0331edf6e07f3a8eb035ff9ce6bfee5c817927b79bf46da92a0689648bc0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1377ba96bc2a27c952f652bd52b12155a6479a8f9bd74522c0d71eb0ed021e16`  
		Last Modified: Sat, 17 Dec 2022 03:06:02 GMT  
		Size: 112.9 MB (112940817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2-sdk`

```console
$ docker pull dart@sha256:2f5be872ec113b108545b05b5d5e6f07ff01eee0cb3d2514d0492d546395b254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7ce70683367f221ea23434d69cdc42ee3f533592f496b5e33f559f7f9014c6ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271946081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcadef020af0bf7e217b539e2e1d22506c5c3977f50558106563c1afdbab4c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0b40a320683da865803676e13fef8e4bdd8ba35925bee685b9249e15365a9`  
		Last Modified: Sat, 17 Dec 2022 02:48:31 GMT  
		Size: 193.3 MB (193296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3ec8df88cc0f722d53ac4ed18cd6a3fb0a49b169dac51dd45f8985f3176a2132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0331edf6e07f3a8eb035ff9ce6bfee5c817927b79bf46da92a0689648bc0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1377ba96bc2a27c952f652bd52b12155a6479a8f9bd74522c0d71eb0ed021e16`  
		Last Modified: Sat, 17 Dec 2022 03:06:02 GMT  
		Size: 112.9 MB (112940817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.18`

```console
$ docker pull dart@sha256:2f5be872ec113b108545b05b5d5e6f07ff01eee0cb3d2514d0492d546395b254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.18` - linux; amd64

```console
$ docker pull dart@sha256:7ce70683367f221ea23434d69cdc42ee3f533592f496b5e33f559f7f9014c6ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271946081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcadef020af0bf7e217b539e2e1d22506c5c3977f50558106563c1afdbab4c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0b40a320683da865803676e13fef8e4bdd8ba35925bee685b9249e15365a9`  
		Last Modified: Sat, 17 Dec 2022 02:48:31 GMT  
		Size: 193.3 MB (193296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3ec8df88cc0f722d53ac4ed18cd6a3fb0a49b169dac51dd45f8985f3176a2132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0331edf6e07f3a8eb035ff9ce6bfee5c817927b79bf46da92a0689648bc0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1377ba96bc2a27c952f652bd52b12155a6479a8f9bd74522c0d71eb0ed021e16`  
		Last Modified: Sat, 17 Dec 2022 03:06:02 GMT  
		Size: 112.9 MB (112940817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.18-sdk`

```console
$ docker pull dart@sha256:2f5be872ec113b108545b05b5d5e6f07ff01eee0cb3d2514d0492d546395b254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.18-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7ce70683367f221ea23434d69cdc42ee3f533592f496b5e33f559f7f9014c6ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271946081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcadef020af0bf7e217b539e2e1d22506c5c3977f50558106563c1afdbab4c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0b40a320683da865803676e13fef8e4bdd8ba35925bee685b9249e15365a9`  
		Last Modified: Sat, 17 Dec 2022 02:48:31 GMT  
		Size: 193.3 MB (193296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3ec8df88cc0f722d53ac4ed18cd6a3fb0a49b169dac51dd45f8985f3176a2132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0331edf6e07f3a8eb035ff9ce6bfee5c817927b79bf46da92a0689648bc0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1377ba96bc2a27c952f652bd52b12155a6479a8f9bd74522c0d71eb0ed021e16`  
		Last Modified: Sat, 17 Dec 2022 03:06:02 GMT  
		Size: 112.9 MB (112940817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.18.6`

```console
$ docker pull dart@sha256:2f5be872ec113b108545b05b5d5e6f07ff01eee0cb3d2514d0492d546395b254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.18.6` - linux; amd64

```console
$ docker pull dart@sha256:7ce70683367f221ea23434d69cdc42ee3f533592f496b5e33f559f7f9014c6ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271946081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcadef020af0bf7e217b539e2e1d22506c5c3977f50558106563c1afdbab4c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0b40a320683da865803676e13fef8e4bdd8ba35925bee685b9249e15365a9`  
		Last Modified: Sat, 17 Dec 2022 02:48:31 GMT  
		Size: 193.3 MB (193296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18.6` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18.6` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3ec8df88cc0f722d53ac4ed18cd6a3fb0a49b169dac51dd45f8985f3176a2132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0331edf6e07f3a8eb035ff9ce6bfee5c817927b79bf46da92a0689648bc0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1377ba96bc2a27c952f652bd52b12155a6479a8f9bd74522c0d71eb0ed021e16`  
		Last Modified: Sat, 17 Dec 2022 03:06:02 GMT  
		Size: 112.9 MB (112940817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.18.6-sdk`

```console
$ docker pull dart@sha256:2f5be872ec113b108545b05b5d5e6f07ff01eee0cb3d2514d0492d546395b254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.18.6-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7ce70683367f221ea23434d69cdc42ee3f533592f496b5e33f559f7f9014c6ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271946081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcadef020af0bf7e217b539e2e1d22506c5c3977f50558106563c1afdbab4c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0b40a320683da865803676e13fef8e4bdd8ba35925bee685b9249e15365a9`  
		Last Modified: Sat, 17 Dec 2022 02:48:31 GMT  
		Size: 193.3 MB (193296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18.6-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.18.6-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3ec8df88cc0f722d53ac4ed18cd6a3fb0a49b169dac51dd45f8985f3176a2132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0331edf6e07f3a8eb035ff9ce6bfee5c817927b79bf46da92a0689648bc0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1377ba96bc2a27c952f652bd52b12155a6479a8f9bd74522c0d71eb0ed021e16`  
		Last Modified: Sat, 17 Dec 2022 03:06:02 GMT  
		Size: 112.9 MB (112940817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19.0-444.2.beta`

```console
$ docker pull dart@sha256:bab342b08fff246c29226f3403e54b69b00316546decd3350c6975fb1480187f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19.0-444.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:a2173fd84e54ccb9da3ef5a472b30bc635be0aff0e63803e63adb4b9139e9f85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1093be4d8ccdf07d096b39dd52dcce024759625fd73d982326534abdec8a7c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aeb05b2b17754e6d74df6224008590605432a5b721fb7bd09651178cf8a456`  
		Last Modified: Sat, 17 Dec 2022 02:49:28 GMT  
		Size: 229.9 MB (229930943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.0-444.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:452338a740655dc5f111eacd98bd9fe475240c22ce4860cd8d67f146691c9d88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204941255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02650998c74ff6f59c8280b09af4742abd28677b579272501a2bb9a26ca3c9a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:01:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dac8d78206a46493fc76fb9bac4a10aca73629c651f8adc104eaab397eb851`  
		Last Modified: Sat, 17 Dec 2022 03:03:42 GMT  
		Size: 136.1 MB (136119967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.0-444.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:236361c04ef6cb2855128c8a74cf7ef9146998ff936acdfb7623d7a155201e4a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214036957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66864e99a49dda68bac84b9a697b5e0f09e53aa96d8ead2686e0d29b82e65210`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9c54b20a90b9dfd2d8451221bb060c4b96d93cedbeaa07f45ddc39df491573`  
		Last Modified: Sat, 17 Dec 2022 03:06:42 GMT  
		Size: 137.4 MB (137418369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19.0-444.2.beta-sdk`

```console
$ docker pull dart@sha256:bab342b08fff246c29226f3403e54b69b00316546decd3350c6975fb1480187f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19.0-444.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a2173fd84e54ccb9da3ef5a472b30bc635be0aff0e63803e63adb4b9139e9f85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1093be4d8ccdf07d096b39dd52dcce024759625fd73d982326534abdec8a7c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aeb05b2b17754e6d74df6224008590605432a5b721fb7bd09651178cf8a456`  
		Last Modified: Sat, 17 Dec 2022 02:49:28 GMT  
		Size: 229.9 MB (229930943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.0-444.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:452338a740655dc5f111eacd98bd9fe475240c22ce4860cd8d67f146691c9d88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204941255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02650998c74ff6f59c8280b09af4742abd28677b579272501a2bb9a26ca3c9a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:01:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dac8d78206a46493fc76fb9bac4a10aca73629c651f8adc104eaab397eb851`  
		Last Modified: Sat, 17 Dec 2022 03:03:42 GMT  
		Size: 136.1 MB (136119967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.0-444.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:236361c04ef6cb2855128c8a74cf7ef9146998ff936acdfb7623d7a155201e4a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214036957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66864e99a49dda68bac84b9a697b5e0f09e53aa96d8ead2686e0d29b82e65210`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9c54b20a90b9dfd2d8451221bb060c4b96d93cedbeaa07f45ddc39df491573`  
		Last Modified: Sat, 17 Dec 2022 03:06:42 GMT  
		Size: 137.4 MB (137418369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:bab342b08fff246c29226f3403e54b69b00316546decd3350c6975fb1480187f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:a2173fd84e54ccb9da3ef5a472b30bc635be0aff0e63803e63adb4b9139e9f85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1093be4d8ccdf07d096b39dd52dcce024759625fd73d982326534abdec8a7c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aeb05b2b17754e6d74df6224008590605432a5b721fb7bd09651178cf8a456`  
		Last Modified: Sat, 17 Dec 2022 02:49:28 GMT  
		Size: 229.9 MB (229930943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:452338a740655dc5f111eacd98bd9fe475240c22ce4860cd8d67f146691c9d88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204941255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02650998c74ff6f59c8280b09af4742abd28677b579272501a2bb9a26ca3c9a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:01:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dac8d78206a46493fc76fb9bac4a10aca73629c651f8adc104eaab397eb851`  
		Last Modified: Sat, 17 Dec 2022 03:03:42 GMT  
		Size: 136.1 MB (136119967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:236361c04ef6cb2855128c8a74cf7ef9146998ff936acdfb7623d7a155201e4a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214036957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66864e99a49dda68bac84b9a697b5e0f09e53aa96d8ead2686e0d29b82e65210`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9c54b20a90b9dfd2d8451221bb060c4b96d93cedbeaa07f45ddc39df491573`  
		Last Modified: Sat, 17 Dec 2022 03:06:42 GMT  
		Size: 137.4 MB (137418369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:bab342b08fff246c29226f3403e54b69b00316546decd3350c6975fb1480187f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a2173fd84e54ccb9da3ef5a472b30bc635be0aff0e63803e63adb4b9139e9f85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1093be4d8ccdf07d096b39dd52dcce024759625fd73d982326534abdec8a7c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aeb05b2b17754e6d74df6224008590605432a5b721fb7bd09651178cf8a456`  
		Last Modified: Sat, 17 Dec 2022 02:49:28 GMT  
		Size: 229.9 MB (229930943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:452338a740655dc5f111eacd98bd9fe475240c22ce4860cd8d67f146691c9d88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204941255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02650998c74ff6f59c8280b09af4742abd28677b579272501a2bb9a26ca3c9a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:01:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dac8d78206a46493fc76fb9bac4a10aca73629c651f8adc104eaab397eb851`  
		Last Modified: Sat, 17 Dec 2022 03:03:42 GMT  
		Size: 136.1 MB (136119967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:236361c04ef6cb2855128c8a74cf7ef9146998ff936acdfb7623d7a155201e4a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214036957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66864e99a49dda68bac84b9a697b5e0f09e53aa96d8ead2686e0d29b82e65210`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9454bfc7eeab61dd7d9b13a393c0c2978ee5a71a2059c687b1b2e8e31eef6740;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8b6d06901fda8603e9d0f91224f8d376ff10079a28491be33d84f5c9fbce816d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b03f47f26373873643e7e7ce85fad3b6fe0220d1707be774288e9b4f1d9beddf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-444.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9c54b20a90b9dfd2d8451221bb060c4b96d93cedbeaa07f45ddc39df491573`  
		Last Modified: Sat, 17 Dec 2022 03:06:42 GMT  
		Size: 137.4 MB (137418369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:2f5be872ec113b108545b05b5d5e6f07ff01eee0cb3d2514d0492d546395b254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:7ce70683367f221ea23434d69cdc42ee3f533592f496b5e33f559f7f9014c6ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271946081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcadef020af0bf7e217b539e2e1d22506c5c3977f50558106563c1afdbab4c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0b40a320683da865803676e13fef8e4bdd8ba35925bee685b9249e15365a9`  
		Last Modified: Sat, 17 Dec 2022 02:48:31 GMT  
		Size: 193.3 MB (193296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3ec8df88cc0f722d53ac4ed18cd6a3fb0a49b169dac51dd45f8985f3176a2132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0331edf6e07f3a8eb035ff9ce6bfee5c817927b79bf46da92a0689648bc0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1377ba96bc2a27c952f652bd52b12155a6479a8f9bd74522c0d71eb0ed021e16`  
		Last Modified: Sat, 17 Dec 2022 03:06:02 GMT  
		Size: 112.9 MB (112940817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:2f5be872ec113b108545b05b5d5e6f07ff01eee0cb3d2514d0492d546395b254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:7ce70683367f221ea23434d69cdc42ee3f533592f496b5e33f559f7f9014c6ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271946081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcadef020af0bf7e217b539e2e1d22506c5c3977f50558106563c1afdbab4c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0b40a320683da865803676e13fef8e4bdd8ba35925bee685b9249e15365a9`  
		Last Modified: Sat, 17 Dec 2022 02:48:31 GMT  
		Size: 193.3 MB (193296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3ec8df88cc0f722d53ac4ed18cd6a3fb0a49b169dac51dd45f8985f3176a2132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0331edf6e07f3a8eb035ff9ce6bfee5c817927b79bf46da92a0689648bc0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1377ba96bc2a27c952f652bd52b12155a6479a8f9bd74522c0d71eb0ed021e16`  
		Last Modified: Sat, 17 Dec 2022 03:06:02 GMT  
		Size: 112.9 MB (112940817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:2f5be872ec113b108545b05b5d5e6f07ff01eee0cb3d2514d0492d546395b254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:7ce70683367f221ea23434d69cdc42ee3f533592f496b5e33f559f7f9014c6ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271946081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcadef020af0bf7e217b539e2e1d22506c5c3977f50558106563c1afdbab4c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0b40a320683da865803676e13fef8e4bdd8ba35925bee685b9249e15365a9`  
		Last Modified: Sat, 17 Dec 2022 02:48:31 GMT  
		Size: 193.3 MB (193296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3ec8df88cc0f722d53ac4ed18cd6a3fb0a49b169dac51dd45f8985f3176a2132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0331edf6e07f3a8eb035ff9ce6bfee5c817927b79bf46da92a0689648bc0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1377ba96bc2a27c952f652bd52b12155a6479a8f9bd74522c0d71eb0ed021e16`  
		Last Modified: Sat, 17 Dec 2022 03:06:02 GMT  
		Size: 112.9 MB (112940817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:2f5be872ec113b108545b05b5d5e6f07ff01eee0cb3d2514d0492d546395b254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7ce70683367f221ea23434d69cdc42ee3f533592f496b5e33f559f7f9014c6ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271946081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcadef020af0bf7e217b539e2e1d22506c5c3977f50558106563c1afdbab4c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:25:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:25:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:25:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:25:23 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:25:24 GMT
WORKDIR /root
# Sat, 17 Dec 2022 02:47:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34df0b3a447c281ea06d9c3e6fd18f26e3005f46600a6c80991d5e097c441`  
		Last Modified: Tue, 06 Dec 2022 02:26:26 GMT  
		Size: 45.1 MB (45074515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e5662a2d3a834429c6d91698e1dc3cc23a6c8366f59c13112620b503c323d`  
		Last Modified: Tue, 06 Dec 2022 02:26:19 GMT  
		Size: 2.2 MB (2162024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0b40a320683da865803676e13fef8e4bdd8ba35925bee685b9249e15365a9`  
		Last Modified: Sat, 17 Dec 2022 02:48:31 GMT  
		Size: 193.3 MB (193296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2d360ee94083fb7a951c62a1983441bfb982a97e2e244cca61da6ec07cafdba8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180607509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7221d08b7e6217647bb8d51885062dd68aac7b60e6e0ed7a2c6ee9a68d19c228`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:18:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:18:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 10:18:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 10:18:48 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 10:18:48 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:00:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ec7cafde80877669de70f264ee7dceb4d0024653bfd07b446d111882c13230`  
		Last Modified: Tue, 06 Dec 2022 10:20:21 GMT  
		Size: 41.0 MB (40956422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2d90e50e263b0a2a9cc22b0b9fdabb6fc02cfd394f8fad51b1ceb1d450d56`  
		Last Modified: Tue, 06 Dec 2022 10:20:14 GMT  
		Size: 1.3 MB (1288518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad75836ddeea1d435c6db7f3d2e2c8ba7ba9ff6ae8b495bb9d98be60e4fb93`  
		Last Modified: Sat, 17 Dec 2022 03:02:41 GMT  
		Size: 111.8 MB (111786221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3ec8df88cc0f722d53ac4ed18cd6a3fb0a49b169dac51dd45f8985f3176a2132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0331edf6e07f3a8eb035ff9ce6bfee5c817927b79bf46da92a0689648bc0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:39:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 06 Dec 2022 02:39:07 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 06 Dec 2022 02:39:07 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 02:39:07 GMT
WORKDIR /root
# Sat, 17 Dec 2022 03:05:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=492c0e835203c4402e3d8291d12b53927f0300c8080aaf63a9113c204255a735;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c360ff64d1306ed5038a7df98142eff832abebc486d3e2b7f68b0fc53279a849;             SDK_ARCH="arm";;         arm64)             DART_SHA256=61dbb462b48aee4f3184b6ecdd356632f39165ae8570fe77a62900a6444f702c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.18.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d917a7e957b7ab720ebce685c3185d778f3797ecab94c98ed8b10e1153a968`  
		Last Modified: Tue, 06 Dec 2022 02:39:57 GMT  
		Size: 45.0 MB (44996085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c0c48988505b5210ac33bb7ef0500bab1289dde272bd14d2ef96f89e6480f1`  
		Last Modified: Tue, 06 Dec 2022 02:39:51 GMT  
		Size: 1.6 MB (1562183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1377ba96bc2a27c952f652bd52b12155a6479a8f9bd74522c0d71eb0ed021e16`  
		Last Modified: Sat, 17 Dec 2022 03:06:02 GMT  
		Size: 112.9 MB (112940817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
