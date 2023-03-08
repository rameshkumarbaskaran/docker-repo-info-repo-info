<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:2`](#dart2)
-	[`dart:2-sdk`](#dart2-sdk)
-	[`dart:2.19`](#dart219)
-	[`dart:2.19-sdk`](#dart219-sdk)
-	[`dart:2.19.4`](#dart2194)
-	[`dart:2.19.4-sdk`](#dart2194-sdk)
-	[`dart:3.0.0-218.1.beta`](#dart300-2181beta)
-	[`dart:3.0.0-218.1.beta-sdk`](#dart300-2181beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:2`

```console
$ docker pull dart@sha256:5d2f42239d719bef7fe60abb37273aea16d8526980662b696c218663ac005d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2` - linux; amd64

```console
$ docker pull dart@sha256:dabe747cc4c44d62d2ce9337a482ce5238965c5c2fa3980d6acc667a8aa1c4c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40e54396ca778d00db1e9cf210bcbc545de26e266a4307bc44861415711f65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4b832ed2b5afc603c17d6a3e86a66a9375655364a3fc66767cb7de0b0b5c4`  
		Last Modified: Wed, 08 Mar 2023 19:20:43 GMT  
		Size: 221.9 MB (221913272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm variant v7

```console
$ docker pull dart@sha256:609d4d52728feaa977573d122f508bbffca2a30de0f388cf77e98807a6ce180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3264d5e28e14c2271c861e03d2fe9cf0cacef6b81d162ddff59b9246f4140c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0b0c5c959e308c5938a53ab55713c9532f9ba8543358c36ac069b3a38c693`  
		Last Modified: Wed, 08 Mar 2023 19:58:56 GMT  
		Size: 127.9 MB (127903417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4212ab6616b992fd3cdd79009f27d4c75ec304d4ca91814196d2f82d5f981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205987120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b78c4830bef627d3407546efbc45aa4399732548715a20c239f206bd60439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:39:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4156da6bde6632660a8a6c95c0df6b9d0c6cd616954975826366695fe8642d23`  
		Last Modified: Wed, 08 Mar 2023 19:40:08 GMT  
		Size: 129.4 MB (129350995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2-sdk`

```console
$ docker pull dart@sha256:5d2f42239d719bef7fe60abb37273aea16d8526980662b696c218663ac005d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:dabe747cc4c44d62d2ce9337a482ce5238965c5c2fa3980d6acc667a8aa1c4c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40e54396ca778d00db1e9cf210bcbc545de26e266a4307bc44861415711f65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4b832ed2b5afc603c17d6a3e86a66a9375655364a3fc66767cb7de0b0b5c4`  
		Last Modified: Wed, 08 Mar 2023 19:20:43 GMT  
		Size: 221.9 MB (221913272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:609d4d52728feaa977573d122f508bbffca2a30de0f388cf77e98807a6ce180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3264d5e28e14c2271c861e03d2fe9cf0cacef6b81d162ddff59b9246f4140c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0b0c5c959e308c5938a53ab55713c9532f9ba8543358c36ac069b3a38c693`  
		Last Modified: Wed, 08 Mar 2023 19:58:56 GMT  
		Size: 127.9 MB (127903417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4212ab6616b992fd3cdd79009f27d4c75ec304d4ca91814196d2f82d5f981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205987120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b78c4830bef627d3407546efbc45aa4399732548715a20c239f206bd60439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:39:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4156da6bde6632660a8a6c95c0df6b9d0c6cd616954975826366695fe8642d23`  
		Last Modified: Wed, 08 Mar 2023 19:40:08 GMT  
		Size: 129.4 MB (129350995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19`

```console
$ docker pull dart@sha256:5d2f42239d719bef7fe60abb37273aea16d8526980662b696c218663ac005d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19` - linux; amd64

```console
$ docker pull dart@sha256:dabe747cc4c44d62d2ce9337a482ce5238965c5c2fa3980d6acc667a8aa1c4c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40e54396ca778d00db1e9cf210bcbc545de26e266a4307bc44861415711f65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4b832ed2b5afc603c17d6a3e86a66a9375655364a3fc66767cb7de0b0b5c4`  
		Last Modified: Wed, 08 Mar 2023 19:20:43 GMT  
		Size: 221.9 MB (221913272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19` - linux; arm variant v7

```console
$ docker pull dart@sha256:609d4d52728feaa977573d122f508bbffca2a30de0f388cf77e98807a6ce180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3264d5e28e14c2271c861e03d2fe9cf0cacef6b81d162ddff59b9246f4140c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0b0c5c959e308c5938a53ab55713c9532f9ba8543358c36ac069b3a38c693`  
		Last Modified: Wed, 08 Mar 2023 19:58:56 GMT  
		Size: 127.9 MB (127903417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4212ab6616b992fd3cdd79009f27d4c75ec304d4ca91814196d2f82d5f981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205987120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b78c4830bef627d3407546efbc45aa4399732548715a20c239f206bd60439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:39:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4156da6bde6632660a8a6c95c0df6b9d0c6cd616954975826366695fe8642d23`  
		Last Modified: Wed, 08 Mar 2023 19:40:08 GMT  
		Size: 129.4 MB (129350995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19-sdk`

```console
$ docker pull dart@sha256:5d2f42239d719bef7fe60abb37273aea16d8526980662b696c218663ac005d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19-sdk` - linux; amd64

```console
$ docker pull dart@sha256:dabe747cc4c44d62d2ce9337a482ce5238965c5c2fa3980d6acc667a8aa1c4c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40e54396ca778d00db1e9cf210bcbc545de26e266a4307bc44861415711f65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4b832ed2b5afc603c17d6a3e86a66a9375655364a3fc66767cb7de0b0b5c4`  
		Last Modified: Wed, 08 Mar 2023 19:20:43 GMT  
		Size: 221.9 MB (221913272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:609d4d52728feaa977573d122f508bbffca2a30de0f388cf77e98807a6ce180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3264d5e28e14c2271c861e03d2fe9cf0cacef6b81d162ddff59b9246f4140c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0b0c5c959e308c5938a53ab55713c9532f9ba8543358c36ac069b3a38c693`  
		Last Modified: Wed, 08 Mar 2023 19:58:56 GMT  
		Size: 127.9 MB (127903417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4212ab6616b992fd3cdd79009f27d4c75ec304d4ca91814196d2f82d5f981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205987120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b78c4830bef627d3407546efbc45aa4399732548715a20c239f206bd60439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:39:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4156da6bde6632660a8a6c95c0df6b9d0c6cd616954975826366695fe8642d23`  
		Last Modified: Wed, 08 Mar 2023 19:40:08 GMT  
		Size: 129.4 MB (129350995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19.4`

```console
$ docker pull dart@sha256:5d2f42239d719bef7fe60abb37273aea16d8526980662b696c218663ac005d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19.4` - linux; amd64

```console
$ docker pull dart@sha256:dabe747cc4c44d62d2ce9337a482ce5238965c5c2fa3980d6acc667a8aa1c4c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40e54396ca778d00db1e9cf210bcbc545de26e266a4307bc44861415711f65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4b832ed2b5afc603c17d6a3e86a66a9375655364a3fc66767cb7de0b0b5c4`  
		Last Modified: Wed, 08 Mar 2023 19:20:43 GMT  
		Size: 221.9 MB (221913272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.4` - linux; arm variant v7

```console
$ docker pull dart@sha256:609d4d52728feaa977573d122f508bbffca2a30de0f388cf77e98807a6ce180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3264d5e28e14c2271c861e03d2fe9cf0cacef6b81d162ddff59b9246f4140c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0b0c5c959e308c5938a53ab55713c9532f9ba8543358c36ac069b3a38c693`  
		Last Modified: Wed, 08 Mar 2023 19:58:56 GMT  
		Size: 127.9 MB (127903417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.4` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4212ab6616b992fd3cdd79009f27d4c75ec304d4ca91814196d2f82d5f981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205987120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b78c4830bef627d3407546efbc45aa4399732548715a20c239f206bd60439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:39:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4156da6bde6632660a8a6c95c0df6b9d0c6cd616954975826366695fe8642d23`  
		Last Modified: Wed, 08 Mar 2023 19:40:08 GMT  
		Size: 129.4 MB (129350995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.19.4-sdk`

```console
$ docker pull dart@sha256:5d2f42239d719bef7fe60abb37273aea16d8526980662b696c218663ac005d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.19.4-sdk` - linux; amd64

```console
$ docker pull dart@sha256:dabe747cc4c44d62d2ce9337a482ce5238965c5c2fa3980d6acc667a8aa1c4c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40e54396ca778d00db1e9cf210bcbc545de26e266a4307bc44861415711f65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4b832ed2b5afc603c17d6a3e86a66a9375655364a3fc66767cb7de0b0b5c4`  
		Last Modified: Wed, 08 Mar 2023 19:20:43 GMT  
		Size: 221.9 MB (221913272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.4-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:609d4d52728feaa977573d122f508bbffca2a30de0f388cf77e98807a6ce180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3264d5e28e14c2271c861e03d2fe9cf0cacef6b81d162ddff59b9246f4140c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0b0c5c959e308c5938a53ab55713c9532f9ba8543358c36ac069b3a38c693`  
		Last Modified: Wed, 08 Mar 2023 19:58:56 GMT  
		Size: 127.9 MB (127903417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.19.4-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4212ab6616b992fd3cdd79009f27d4c75ec304d4ca91814196d2f82d5f981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205987120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b78c4830bef627d3407546efbc45aa4399732548715a20c239f206bd60439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:39:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4156da6bde6632660a8a6c95c0df6b9d0c6cd616954975826366695fe8642d23`  
		Last Modified: Wed, 08 Mar 2023 19:40:08 GMT  
		Size: 129.4 MB (129350995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.0.0-218.1.beta`

```console
$ docker pull dart@sha256:ea3a949da39c1bd733bbc94ba75b515df95ee2005f1e7075cdfbd13bb04dfb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.0.0-218.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:c2d7342855cfbddec61d47b95842cb1c0a5f8ad0bd6ba925dba719d69f4a2f83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289396307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f9e53f5e600d9cd152c6ccdf61334319ef2b9f2c56ff6f33dc8d3440c112a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 01 Mar 2023 05:00:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798e157d2369ed7d42a0f0c34a2b62baf15f37d4f4bd185bcd27226dc5880bc7`  
		Last Modified: Wed, 01 Mar 2023 05:02:28 GMT  
		Size: 210.7 MB (210721117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.0.0-218.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:6d806a0bb83f35a33e2990c773809f2aa3106c426ec8eea28919ec4cf313b513
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185636580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e956e01991a585fda5e476d4cd356b0047200777a0f7d59397ba3ce910948eba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 01 Mar 2023 02:25:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffca9a03c3582f37111d344630f964ea92015e08ced51e594944f16a2e1379ac`  
		Last Modified: Wed, 01 Mar 2023 02:27:36 GMT  
		Size: 116.8 MB (116782123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.0.0-218.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7e3aa605644df91c4ec2b4785bcf68906e7497d34693338fa5ef8e500b3f8cad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194583316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554a5ed060eb7115771eca2f5970938382a7cbf481dcd9f76d119dadd0a3b20b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 01 Mar 2023 13:04:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38287c01af1302b8309848418b64826284fac1ab11168e8dcf59891fc216d8`  
		Last Modified: Wed, 01 Mar 2023 13:05:32 GMT  
		Size: 117.9 MB (117947191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.0.0-218.1.beta-sdk`

```console
$ docker pull dart@sha256:ea3a949da39c1bd733bbc94ba75b515df95ee2005f1e7075cdfbd13bb04dfb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.0.0-218.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:c2d7342855cfbddec61d47b95842cb1c0a5f8ad0bd6ba925dba719d69f4a2f83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289396307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f9e53f5e600d9cd152c6ccdf61334319ef2b9f2c56ff6f33dc8d3440c112a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 01 Mar 2023 05:00:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798e157d2369ed7d42a0f0c34a2b62baf15f37d4f4bd185bcd27226dc5880bc7`  
		Last Modified: Wed, 01 Mar 2023 05:02:28 GMT  
		Size: 210.7 MB (210721117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.0.0-218.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6d806a0bb83f35a33e2990c773809f2aa3106c426ec8eea28919ec4cf313b513
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185636580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e956e01991a585fda5e476d4cd356b0047200777a0f7d59397ba3ce910948eba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 01 Mar 2023 02:25:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffca9a03c3582f37111d344630f964ea92015e08ced51e594944f16a2e1379ac`  
		Last Modified: Wed, 01 Mar 2023 02:27:36 GMT  
		Size: 116.8 MB (116782123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.0.0-218.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7e3aa605644df91c4ec2b4785bcf68906e7497d34693338fa5ef8e500b3f8cad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194583316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554a5ed060eb7115771eca2f5970938382a7cbf481dcd9f76d119dadd0a3b20b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 01 Mar 2023 13:04:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38287c01af1302b8309848418b64826284fac1ab11168e8dcf59891fc216d8`  
		Last Modified: Wed, 01 Mar 2023 13:05:32 GMT  
		Size: 117.9 MB (117947191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:ea3a949da39c1bd733bbc94ba75b515df95ee2005f1e7075cdfbd13bb04dfb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:c2d7342855cfbddec61d47b95842cb1c0a5f8ad0bd6ba925dba719d69f4a2f83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289396307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f9e53f5e600d9cd152c6ccdf61334319ef2b9f2c56ff6f33dc8d3440c112a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 01 Mar 2023 05:00:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798e157d2369ed7d42a0f0c34a2b62baf15f37d4f4bd185bcd27226dc5880bc7`  
		Last Modified: Wed, 01 Mar 2023 05:02:28 GMT  
		Size: 210.7 MB (210721117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:6d806a0bb83f35a33e2990c773809f2aa3106c426ec8eea28919ec4cf313b513
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185636580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e956e01991a585fda5e476d4cd356b0047200777a0f7d59397ba3ce910948eba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 01 Mar 2023 02:25:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffca9a03c3582f37111d344630f964ea92015e08ced51e594944f16a2e1379ac`  
		Last Modified: Wed, 01 Mar 2023 02:27:36 GMT  
		Size: 116.8 MB (116782123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7e3aa605644df91c4ec2b4785bcf68906e7497d34693338fa5ef8e500b3f8cad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194583316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554a5ed060eb7115771eca2f5970938382a7cbf481dcd9f76d119dadd0a3b20b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 01 Mar 2023 13:04:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38287c01af1302b8309848418b64826284fac1ab11168e8dcf59891fc216d8`  
		Last Modified: Wed, 01 Mar 2023 13:05:32 GMT  
		Size: 117.9 MB (117947191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:ea3a949da39c1bd733bbc94ba75b515df95ee2005f1e7075cdfbd13bb04dfb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:c2d7342855cfbddec61d47b95842cb1c0a5f8ad0bd6ba925dba719d69f4a2f83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289396307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f9e53f5e600d9cd152c6ccdf61334319ef2b9f2c56ff6f33dc8d3440c112a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 01 Mar 2023 05:00:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798e157d2369ed7d42a0f0c34a2b62baf15f37d4f4bd185bcd27226dc5880bc7`  
		Last Modified: Wed, 01 Mar 2023 05:02:28 GMT  
		Size: 210.7 MB (210721117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6d806a0bb83f35a33e2990c773809f2aa3106c426ec8eea28919ec4cf313b513
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185636580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e956e01991a585fda5e476d4cd356b0047200777a0f7d59397ba3ce910948eba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 01 Mar 2023 02:25:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffca9a03c3582f37111d344630f964ea92015e08ced51e594944f16a2e1379ac`  
		Last Modified: Wed, 01 Mar 2023 02:27:36 GMT  
		Size: 116.8 MB (116782123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7e3aa605644df91c4ec2b4785bcf68906e7497d34693338fa5ef8e500b3f8cad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194583316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554a5ed060eb7115771eca2f5970938382a7cbf481dcd9f76d119dadd0a3b20b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 01 Mar 2023 13:04:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=da65d6733d9cca10f04cf981c97f3af7835e51afda84dce73f2e6fea8848c21b;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edea02e68ca5d6becbc58c1b70d378ad4b656f2832530cd57a2fb235aad5829;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b0cd5dacc35e56ca569125a0cdab4539580465a4c0f820311c3f7e22e6f817b4;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.0.0-218.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38287c01af1302b8309848418b64826284fac1ab11168e8dcf59891fc216d8`  
		Last Modified: Wed, 01 Mar 2023 13:05:32 GMT  
		Size: 117.9 MB (117947191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:5d2f42239d719bef7fe60abb37273aea16d8526980662b696c218663ac005d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:dabe747cc4c44d62d2ce9337a482ce5238965c5c2fa3980d6acc667a8aa1c4c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40e54396ca778d00db1e9cf210bcbc545de26e266a4307bc44861415711f65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4b832ed2b5afc603c17d6a3e86a66a9375655364a3fc66767cb7de0b0b5c4`  
		Last Modified: Wed, 08 Mar 2023 19:20:43 GMT  
		Size: 221.9 MB (221913272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:609d4d52728feaa977573d122f508bbffca2a30de0f388cf77e98807a6ce180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3264d5e28e14c2271c861e03d2fe9cf0cacef6b81d162ddff59b9246f4140c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0b0c5c959e308c5938a53ab55713c9532f9ba8543358c36ac069b3a38c693`  
		Last Modified: Wed, 08 Mar 2023 19:58:56 GMT  
		Size: 127.9 MB (127903417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4212ab6616b992fd3cdd79009f27d4c75ec304d4ca91814196d2f82d5f981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205987120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b78c4830bef627d3407546efbc45aa4399732548715a20c239f206bd60439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:39:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4156da6bde6632660a8a6c95c0df6b9d0c6cd616954975826366695fe8642d23`  
		Last Modified: Wed, 08 Mar 2023 19:40:08 GMT  
		Size: 129.4 MB (129350995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:5d2f42239d719bef7fe60abb37273aea16d8526980662b696c218663ac005d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:dabe747cc4c44d62d2ce9337a482ce5238965c5c2fa3980d6acc667a8aa1c4c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40e54396ca778d00db1e9cf210bcbc545de26e266a4307bc44861415711f65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4b832ed2b5afc603c17d6a3e86a66a9375655364a3fc66767cb7de0b0b5c4`  
		Last Modified: Wed, 08 Mar 2023 19:20:43 GMT  
		Size: 221.9 MB (221913272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:609d4d52728feaa977573d122f508bbffca2a30de0f388cf77e98807a6ce180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3264d5e28e14c2271c861e03d2fe9cf0cacef6b81d162ddff59b9246f4140c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0b0c5c959e308c5938a53ab55713c9532f9ba8543358c36ac069b3a38c693`  
		Last Modified: Wed, 08 Mar 2023 19:58:56 GMT  
		Size: 127.9 MB (127903417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4212ab6616b992fd3cdd79009f27d4c75ec304d4ca91814196d2f82d5f981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205987120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b78c4830bef627d3407546efbc45aa4399732548715a20c239f206bd60439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:39:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4156da6bde6632660a8a6c95c0df6b9d0c6cd616954975826366695fe8642d23`  
		Last Modified: Wed, 08 Mar 2023 19:40:08 GMT  
		Size: 129.4 MB (129350995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:5d2f42239d719bef7fe60abb37273aea16d8526980662b696c218663ac005d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:dabe747cc4c44d62d2ce9337a482ce5238965c5c2fa3980d6acc667a8aa1c4c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40e54396ca778d00db1e9cf210bcbc545de26e266a4307bc44861415711f65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4b832ed2b5afc603c17d6a3e86a66a9375655364a3fc66767cb7de0b0b5c4`  
		Last Modified: Wed, 08 Mar 2023 19:20:43 GMT  
		Size: 221.9 MB (221913272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:609d4d52728feaa977573d122f508bbffca2a30de0f388cf77e98807a6ce180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3264d5e28e14c2271c861e03d2fe9cf0cacef6b81d162ddff59b9246f4140c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0b0c5c959e308c5938a53ab55713c9532f9ba8543358c36ac069b3a38c693`  
		Last Modified: Wed, 08 Mar 2023 19:58:56 GMT  
		Size: 127.9 MB (127903417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4212ab6616b992fd3cdd79009f27d4c75ec304d4ca91814196d2f82d5f981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205987120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b78c4830bef627d3407546efbc45aa4399732548715a20c239f206bd60439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:39:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4156da6bde6632660a8a6c95c0df6b9d0c6cd616954975826366695fe8642d23`  
		Last Modified: Wed, 08 Mar 2023 19:40:08 GMT  
		Size: 129.4 MB (129350995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:5d2f42239d719bef7fe60abb37273aea16d8526980662b696c218663ac005d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:dabe747cc4c44d62d2ce9337a482ce5238965c5c2fa3980d6acc667a8aa1c4c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40e54396ca778d00db1e9cf210bcbc545de26e266a4307bc44861415711f65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 05:00:11 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 05:00:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:00:11 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc65615115efc0214c3c9c0c85199857a0ddff5901bbc028bfa2dd6156d5fe5`  
		Last Modified: Wed, 01 Mar 2023 05:01:13 GMT  
		Size: 45.1 MB (45101765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcbccd766aa06004906194a9d2e07d3e01d1791d99edf901dda9e0ab3f0b415`  
		Last Modified: Wed, 01 Mar 2023 05:01:06 GMT  
		Size: 2.2 MB (2162022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4b832ed2b5afc603c17d6a3e86a66a9375655364a3fc66767cb7de0b0b5c4`  
		Last Modified: Wed, 08 Mar 2023 19:20:43 GMT  
		Size: 221.9 MB (221913272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:609d4d52728feaa977573d122f508bbffca2a30de0f388cf77e98807a6ce180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3264d5e28e14c2271c861e03d2fe9cf0cacef6b81d162ddff59b9246f4140c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:25:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:25:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 02:25:08 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 02:25:08 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 02:25:08 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a2a2202be4ce8d1e3c64eeb5cd1a880b653007a431bebfcb9aa6b27ac927e`  
		Last Modified: Wed, 01 Mar 2023 02:26:29 GMT  
		Size: 41.0 MB (40988626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2c1c5227941118e0a1f640f63b2b993bb7b3e42883849a783c7f7cd6d4487`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 1.3 MB (1288541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0b0c5c959e308c5938a53ab55713c9532f9ba8543358c36ac069b3a38c693`  
		Last Modified: Wed, 08 Mar 2023 19:58:56 GMT  
		Size: 127.9 MB (127903417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4212ab6616b992fd3cdd79009f27d4c75ec304d4ca91814196d2f82d5f981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205987120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b78c4830bef627d3407546efbc45aa4399732548715a20c239f206bd60439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:03:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Mar 2023 13:03:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Mar 2023 13:03:50 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:03:50 GMT
WORKDIR /root
# Wed, 08 Mar 2023 19:39:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f8591944512834ba19b4d8383d270d7f56fef03c56ba53d4e35c23db80ea8a33;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a87833fbfed26ef810cb135c47eb7b5bc24c906b55abb4a2e183fea2d3ce1b51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c81303feea24228148bd4ec14c65bb9c341cba3596e3d68e8a874a9df947f928;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.19.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bad58cbb76aa261586e238ac663c806e6da6fda3059b45385c8c3938a59387`  
		Last Modified: Wed, 01 Mar 2023 13:04:43 GMT  
		Size: 45.0 MB (45011137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f122052879f43039ebbbbe28f2f87037e49d388f36058bf9b4f1e579229b1a`  
		Last Modified: Wed, 01 Mar 2023 13:04:38 GMT  
		Size: 1.6 MB (1562174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4156da6bde6632660a8a6c95c0df6b9d0c6cd616954975826366695fe8642d23`  
		Last Modified: Wed, 08 Mar 2023 19:40:08 GMT  
		Size: 129.4 MB (129350995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
