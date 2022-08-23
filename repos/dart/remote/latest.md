## `dart:latest`

```console
$ docker pull dart@sha256:f45a3d42f0b69138a7f1a46ecfbe00db80ef3bd09809c066adcee69e2d96385a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:6b78da28e8f0a690b8f6572b840916455390acb9206c21c56806d23797ace02c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275834105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4030ca6dbb484ed322b14c0d447defe746efb0d435effe0fe7767ae9eb84270`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:02:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:02:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 23 Aug 2022 01:02:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 23 Aug 2022 01:02:52 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 01:02:52 GMT
WORKDIR /root
# Tue, 23 Aug 2022 01:03:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f837f385603a1cfb14ddb7dd0cd64820b297646626bdb689ccfc3278fa83b2b1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3eae7ed5773c125165d123a235bac9956981cfdf164059806ed69a6feefc1eda;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8e71b0c958a587c83ecd6c8cc637bc624bb85bc64e877e9ea00831a659a904b1;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.17.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb560d52a31acbd32a4f357b69ca8a95b39c44794c8288e569a2843a7abdadd`  
		Last Modified: Tue, 23 Aug 2022 01:03:49 GMT  
		Size: 45.1 MB (45075989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fc341668ed4edfe9e06de856dffd63709856fad6a289de2992c44997673876`  
		Last Modified: Tue, 23 Aug 2022 01:03:42 GMT  
		Size: 2.1 MB (2139552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033dbe532fe7349ae81342bde4e444e47e288dfda66108155579ff4f0cf6beb2`  
		Last Modified: Tue, 23 Aug 2022 01:04:11 GMT  
		Size: 197.2 MB (197237079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:e3cbe50f63bb282f9de1181a5e40a9d4fa21d19883d8897929a260032a25d6e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184071733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e1b844a8f2b49aa18bc54c7a187e20f29bdca869d4469b34369cea5b4a6a65`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:20:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:20:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 02 Aug 2022 02:20:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Aug 2022 02:20:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 02:20:49 GMT
WORKDIR /root
# Tue, 02 Aug 2022 02:21:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f837f385603a1cfb14ddb7dd0cd64820b297646626bdb689ccfc3278fa83b2b1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3eae7ed5773c125165d123a235bac9956981cfdf164059806ed69a6feefc1eda;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8e71b0c958a587c83ecd6c8cc637bc624bb85bc64e877e9ea00831a659a904b1;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.17.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8a20881befe196e0cdcccddb3e35696f70d8149cfb4890d204dc9e61d560eb`  
		Last Modified: Tue, 02 Aug 2022 02:22:21 GMT  
		Size: 41.0 MB (40965013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be02c98a86477df0fe47387c314ae22c41a84e22d9351c25fbf9ce29c21b7a24`  
		Last Modified: Tue, 02 Aug 2022 02:22:10 GMT  
		Size: 1.3 MB (1288073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a904479d12ad41c34d9fdce05ebb7f1502e55840a8ebd176d23886605d5b8f34`  
		Last Modified: Tue, 02 Aug 2022 02:22:37 GMT  
		Size: 115.3 MB (115258061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:673962a060306ddf69008be5341ad00691d634b6317dc93d531bc68ae8753167
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193153430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36033e93cf708c130935b762cca09b4000edd2bacf664ff0341ad02714a44861`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:45:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:45:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 23 Aug 2022 02:45:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 23 Aug 2022 02:45:13 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 02:45:14 GMT
WORKDIR /root
# Tue, 23 Aug 2022 02:45:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f837f385603a1cfb14ddb7dd0cd64820b297646626bdb689ccfc3278fa83b2b1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3eae7ed5773c125165d123a235bac9956981cfdf164059806ed69a6feefc1eda;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8e71b0c958a587c83ecd6c8cc637bc624bb85bc64e877e9ea00831a659a904b1;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.17.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c70daf8007713a8a9d33c825885754e7cfa4c68eec5ea6a5c402777d0b9a80b`  
		Last Modified: Tue, 23 Aug 2022 02:46:22 GMT  
		Size: 44.8 MB (44798419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3456734c399cd46ed73bdaec58c27712844f78746f5e9561939cdf1a330f31`  
		Last Modified: Tue, 23 Aug 2022 02:46:16 GMT  
		Size: 1.6 MB (1556733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2f0085fc5d76b685f89412a95e5ac7bb3aebab7efb54b2468743f03a4596ee`  
		Last Modified: Tue, 23 Aug 2022 02:46:32 GMT  
		Size: 116.7 MB (116734490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
