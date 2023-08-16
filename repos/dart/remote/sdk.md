## `dart:sdk`

```console
$ docker pull dart@sha256:3e69d201d73960f8a7e6fb0ee7467ade1495659676a7c09353a39fdb77852b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:d04faa9da103974a42a73915ba28f443aa3430b39656469bf95caa15f4506db5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296613757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7e005e696996ffd7f611ec502bf9f115806d620c0f1fc0f088dd994b10cbf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:57:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:57:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 28 Jul 2023 00:57:24 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 28 Jul 2023 00:57:25 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 00:57:25 GMT
WORKDIR /root
# Fri, 28 Jul 2023 00:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cccd5300faa5a9abce12a5f77586e26350028cea82bb4ff8eeb55641b58a2e1d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a15d42cb1677ac5e50a23045cafe3bf5db2855a5287a3e9019b849fe8477897;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2c8eeaf0d3da60c4e14beec45ce3b39aca754f71b9fa3fb0c635ee28d6f44708;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f327e85d0d085fa1b66e19f223e26d295b0112f5b3118b186eedd566e3cbe4a`  
		Last Modified: Fri, 28 Jul 2023 00:58:22 GMT  
		Size: 45.1 MB (45101672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da22ff9cae25bc9894d49f8004c09cacc8c88a7125b197633206cbdfaaee088`  
		Last Modified: Fri, 28 Jul 2023 00:58:16 GMT  
		Size: 2.2 MB (2160697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f02fff62812e055e6557c81eb1ca0d0726af9da10708d7d23671e2c0dd4c6`  
		Last Modified: Fri, 28 Jul 2023 00:58:43 GMT  
		Size: 217.9 MB (217933786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6c532fcde08cd3645d8210f682d183a4ae4664c91eeae0a7076514780dc99d17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191284063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af009fac56f668ce82a2b90afbc0ad264c5069bfb9478135196d91a94204e8c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:58:18 GMT
ADD file:480cada6975fa477736805a1834cca05d1e18de255c6cc0cca13df01fdb44253 in / 
# Thu, 27 Jul 2023 23:58:18 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:55:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 28 Jul 2023 01:55:27 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 28 Jul 2023 01:55:27 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 01:55:27 GMT
WORKDIR /root
# Fri, 28 Jul 2023 01:55:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cccd5300faa5a9abce12a5f77586e26350028cea82bb4ff8eeb55641b58a2e1d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a15d42cb1677ac5e50a23045cafe3bf5db2855a5287a3e9019b849fe8477897;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2c8eeaf0d3da60c4e14beec45ce3b39aca754f71b9fa3fb0c635ee28d6f44708;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1236490553984befd7be19a151a0489729a35a66c4aaf5d799cd87d2c738371a`  
		Last Modified: Fri, 28 Jul 2023 00:03:56 GMT  
		Size: 26.6 MB (26578603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7323e5a974514854e652831281e0fd7bd1d80513b94656cb181796634cc819f4`  
		Last Modified: Fri, 28 Jul 2023 01:56:17 GMT  
		Size: 41.0 MB (40988395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183ec55d0b3582530c58a4c9ca20596e636b9679a53bcc4a10af114cdb53f25b`  
		Last Modified: Fri, 28 Jul 2023 01:56:11 GMT  
		Size: 1.3 MB (1287725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e92c96224b5c4c0d1752d9c4586fd46b04c1894af6dac7b40937da7fcd5201`  
		Last Modified: Fri, 28 Jul 2023 01:56:29 GMT  
		Size: 122.4 MB (122429340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:51e781b740af0410530dad0506b49996c0ff86910a46b046508c9524504b7a70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200470358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7f32ce104eff0279dd854cfca080cfad9d8dd710ec7ce22f0e1b96b688fb55`
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
# Wed, 16 Aug 2023 02:02:18 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 02:02:18 GMT
WORKDIR /root
# Wed, 16 Aug 2023 02:02:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cccd5300faa5a9abce12a5f77586e26350028cea82bb4ff8eeb55641b58a2e1d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a15d42cb1677ac5e50a23045cafe3bf5db2855a5287a3e9019b849fe8477897;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2c8eeaf0d3da60c4e14beec45ce3b39aca754f71b9fa3fb0c635ee28d6f44708;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:a1ede57bd6e038ca0ce144ad9aae5ad5de09f3d1b1557266f9abe4d1cdbd7487`  
		Last Modified: Wed, 16 Aug 2023 02:03:08 GMT  
		Size: 123.8 MB (123834773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
