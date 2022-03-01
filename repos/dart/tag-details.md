<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:2`](#dart2)
-	[`dart:2-sdk`](#dart2-sdk)
-	[`dart:2.16`](#dart216)
-	[`dart:2.16-sdk`](#dart216-sdk)
-	[`dart:2.16.1`](#dart2161)
-	[`dart:2.16.1-sdk`](#dart2161-sdk)
-	[`dart:2.17.0-69.2.beta`](#dart2170-692beta)
-	[`dart:2.17.0-69.2.beta-sdk`](#dart2170-692beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:2`

```console
$ docker pull dart@sha256:bc3c01156859d85e2e343d9bb87cf57a193dc709d8c9adecdcf71df0b0728704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2` - linux; amd64

```console
$ docker pull dart@sha256:7c9216dd7d7941bdcca30a1e800b821894975a86e12c67c28a1e3b1989241d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279599415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966378310e8018866671cdeee1149e820d022abf972eccd357a66c2572c9a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b98a0af9ec88db1c6cfc7ae0f2abd20871aa1f0c667cc9ff13906f2e26d27d`  
		Last Modified: Tue, 01 Mar 2022 06:48:27 GMT  
		Size: 201.0 MB (201020228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm variant v7

```console
$ docker pull dart@sha256:27562f177904bb9c3168ef2c05e761f9253a2c680c1a7a182fb9bd7a7aed8026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187003363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c21651f2a5da4694eefd119768e6db134f1f5ff13ca63c3e3e1e5665f325b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a6a6f6e6609c4abad1d4eb06bd2d4478ab5751d588434f94eaa420cd39d93`  
		Last Modified: Tue, 01 Mar 2022 10:14:30 GMT  
		Size: 118.2 MB (118185999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d318eb926d57fba2dff37583ed20753c4bc63dff132fb8e19f17fe70e31e12b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e33d608bb95be43cd6802ea19fd735d1fd9a5bfc814a2d0ab18f48f02acaa7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a15e3b36348a88307d515493428151bc89ed71317d490a58b0fdda9260be91`  
		Last Modified: Tue, 01 Mar 2022 10:59:47 GMT  
		Size: 119.7 MB (119699694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2-sdk`

```console
$ docker pull dart@sha256:bc3c01156859d85e2e343d9bb87cf57a193dc709d8c9adecdcf71df0b0728704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7c9216dd7d7941bdcca30a1e800b821894975a86e12c67c28a1e3b1989241d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279599415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966378310e8018866671cdeee1149e820d022abf972eccd357a66c2572c9a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b98a0af9ec88db1c6cfc7ae0f2abd20871aa1f0c667cc9ff13906f2e26d27d`  
		Last Modified: Tue, 01 Mar 2022 06:48:27 GMT  
		Size: 201.0 MB (201020228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:27562f177904bb9c3168ef2c05e761f9253a2c680c1a7a182fb9bd7a7aed8026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187003363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c21651f2a5da4694eefd119768e6db134f1f5ff13ca63c3e3e1e5665f325b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a6a6f6e6609c4abad1d4eb06bd2d4478ab5751d588434f94eaa420cd39d93`  
		Last Modified: Tue, 01 Mar 2022 10:14:30 GMT  
		Size: 118.2 MB (118185999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d318eb926d57fba2dff37583ed20753c4bc63dff132fb8e19f17fe70e31e12b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e33d608bb95be43cd6802ea19fd735d1fd9a5bfc814a2d0ab18f48f02acaa7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a15e3b36348a88307d515493428151bc89ed71317d490a58b0fdda9260be91`  
		Last Modified: Tue, 01 Mar 2022 10:59:47 GMT  
		Size: 119.7 MB (119699694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16`

```console
$ docker pull dart@sha256:bc3c01156859d85e2e343d9bb87cf57a193dc709d8c9adecdcf71df0b0728704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.16` - linux; amd64

```console
$ docker pull dart@sha256:7c9216dd7d7941bdcca30a1e800b821894975a86e12c67c28a1e3b1989241d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279599415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966378310e8018866671cdeee1149e820d022abf972eccd357a66c2572c9a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b98a0af9ec88db1c6cfc7ae0f2abd20871aa1f0c667cc9ff13906f2e26d27d`  
		Last Modified: Tue, 01 Mar 2022 06:48:27 GMT  
		Size: 201.0 MB (201020228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16` - linux; arm variant v7

```console
$ docker pull dart@sha256:27562f177904bb9c3168ef2c05e761f9253a2c680c1a7a182fb9bd7a7aed8026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187003363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c21651f2a5da4694eefd119768e6db134f1f5ff13ca63c3e3e1e5665f325b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a6a6f6e6609c4abad1d4eb06bd2d4478ab5751d588434f94eaa420cd39d93`  
		Last Modified: Tue, 01 Mar 2022 10:14:30 GMT  
		Size: 118.2 MB (118185999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d318eb926d57fba2dff37583ed20753c4bc63dff132fb8e19f17fe70e31e12b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e33d608bb95be43cd6802ea19fd735d1fd9a5bfc814a2d0ab18f48f02acaa7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a15e3b36348a88307d515493428151bc89ed71317d490a58b0fdda9260be91`  
		Last Modified: Tue, 01 Mar 2022 10:59:47 GMT  
		Size: 119.7 MB (119699694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16-sdk`

```console
$ docker pull dart@sha256:bc3c01156859d85e2e343d9bb87cf57a193dc709d8c9adecdcf71df0b0728704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.16-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7c9216dd7d7941bdcca30a1e800b821894975a86e12c67c28a1e3b1989241d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279599415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966378310e8018866671cdeee1149e820d022abf972eccd357a66c2572c9a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b98a0af9ec88db1c6cfc7ae0f2abd20871aa1f0c667cc9ff13906f2e26d27d`  
		Last Modified: Tue, 01 Mar 2022 06:48:27 GMT  
		Size: 201.0 MB (201020228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:27562f177904bb9c3168ef2c05e761f9253a2c680c1a7a182fb9bd7a7aed8026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187003363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c21651f2a5da4694eefd119768e6db134f1f5ff13ca63c3e3e1e5665f325b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a6a6f6e6609c4abad1d4eb06bd2d4478ab5751d588434f94eaa420cd39d93`  
		Last Modified: Tue, 01 Mar 2022 10:14:30 GMT  
		Size: 118.2 MB (118185999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d318eb926d57fba2dff37583ed20753c4bc63dff132fb8e19f17fe70e31e12b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e33d608bb95be43cd6802ea19fd735d1fd9a5bfc814a2d0ab18f48f02acaa7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a15e3b36348a88307d515493428151bc89ed71317d490a58b0fdda9260be91`  
		Last Modified: Tue, 01 Mar 2022 10:59:47 GMT  
		Size: 119.7 MB (119699694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16.1`

```console
$ docker pull dart@sha256:bc3c01156859d85e2e343d9bb87cf57a193dc709d8c9adecdcf71df0b0728704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.16.1` - linux; amd64

```console
$ docker pull dart@sha256:7c9216dd7d7941bdcca30a1e800b821894975a86e12c67c28a1e3b1989241d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279599415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966378310e8018866671cdeee1149e820d022abf972eccd357a66c2572c9a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b98a0af9ec88db1c6cfc7ae0f2abd20871aa1f0c667cc9ff13906f2e26d27d`  
		Last Modified: Tue, 01 Mar 2022 06:48:27 GMT  
		Size: 201.0 MB (201020228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:27562f177904bb9c3168ef2c05e761f9253a2c680c1a7a182fb9bd7a7aed8026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187003363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c21651f2a5da4694eefd119768e6db134f1f5ff13ca63c3e3e1e5665f325b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a6a6f6e6609c4abad1d4eb06bd2d4478ab5751d588434f94eaa420cd39d93`  
		Last Modified: Tue, 01 Mar 2022 10:14:30 GMT  
		Size: 118.2 MB (118185999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d318eb926d57fba2dff37583ed20753c4bc63dff132fb8e19f17fe70e31e12b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e33d608bb95be43cd6802ea19fd735d1fd9a5bfc814a2d0ab18f48f02acaa7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a15e3b36348a88307d515493428151bc89ed71317d490a58b0fdda9260be91`  
		Last Modified: Tue, 01 Mar 2022 10:59:47 GMT  
		Size: 119.7 MB (119699694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16.1-sdk`

```console
$ docker pull dart@sha256:bc3c01156859d85e2e343d9bb87cf57a193dc709d8c9adecdcf71df0b0728704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.16.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7c9216dd7d7941bdcca30a1e800b821894975a86e12c67c28a1e3b1989241d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279599415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966378310e8018866671cdeee1149e820d022abf972eccd357a66c2572c9a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b98a0af9ec88db1c6cfc7ae0f2abd20871aa1f0c667cc9ff13906f2e26d27d`  
		Last Modified: Tue, 01 Mar 2022 06:48:27 GMT  
		Size: 201.0 MB (201020228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:27562f177904bb9c3168ef2c05e761f9253a2c680c1a7a182fb9bd7a7aed8026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187003363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c21651f2a5da4694eefd119768e6db134f1f5ff13ca63c3e3e1e5665f325b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a6a6f6e6609c4abad1d4eb06bd2d4478ab5751d588434f94eaa420cd39d93`  
		Last Modified: Tue, 01 Mar 2022 10:14:30 GMT  
		Size: 118.2 MB (118185999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.16.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d318eb926d57fba2dff37583ed20753c4bc63dff132fb8e19f17fe70e31e12b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e33d608bb95be43cd6802ea19fd735d1fd9a5bfc814a2d0ab18f48f02acaa7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a15e3b36348a88307d515493428151bc89ed71317d490a58b0fdda9260be91`  
		Last Modified: Tue, 01 Mar 2022 10:59:47 GMT  
		Size: 119.7 MB (119699694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.17.0-69.2.beta`

```console
$ docker pull dart@sha256:cb559423dd7d079644b2f4ae1842caae74dca530ae2e4e0e8abdf1dfd84faf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.17.0-69.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:b6dc24d2c05f7d7cdf0fcef7623da367f80d969349a3bca84f1bcdaebe91a9a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276439933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236574319f693fcea39779860b3703709e1fe3b29632860ced1649ca8b27081a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4b760d756a522da3e617513717044b6a609d151ac78e1092690ab7c617a7d3`  
		Last Modified: Tue, 01 Mar 2022 06:49:33 GMT  
		Size: 197.9 MB (197860746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.17.0-69.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:ab9b65cd0a23e10a0081cdd610804dc2417602f9bcbbb72d89949613e45c5ef0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186002276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ac4c840f6887445c83649eed9c4fb2cf106c4e3acce5605d5a9a4179c1eddf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0412307fde17a5db36baf1ad1d2b2792d72fa90b3e4a45c8035ddc2d882f8b`  
		Last Modified: Tue, 01 Mar 2022 10:16:30 GMT  
		Size: 117.2 MB (117184912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.17.0-69.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:713ebf05b46b0285e92044ef34022a6cd5bd0191baf4f9bf70537b995a846c3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195295058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d0c08ded51d40c0c24e0ebf77dc949d48f5e3eb670c15b784bd9472c073e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791e7c6030ac15126eefe586e9095bd5b6b0e7ae2f1808b6dda90eab66c9575e`  
		Last Modified: Tue, 01 Mar 2022 11:00:42 GMT  
		Size: 118.7 MB (118686392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.17.0-69.2.beta-sdk`

```console
$ docker pull dart@sha256:cb559423dd7d079644b2f4ae1842caae74dca530ae2e4e0e8abdf1dfd84faf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.17.0-69.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b6dc24d2c05f7d7cdf0fcef7623da367f80d969349a3bca84f1bcdaebe91a9a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276439933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236574319f693fcea39779860b3703709e1fe3b29632860ced1649ca8b27081a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4b760d756a522da3e617513717044b6a609d151ac78e1092690ab7c617a7d3`  
		Last Modified: Tue, 01 Mar 2022 06:49:33 GMT  
		Size: 197.9 MB (197860746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.17.0-69.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:ab9b65cd0a23e10a0081cdd610804dc2417602f9bcbbb72d89949613e45c5ef0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186002276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ac4c840f6887445c83649eed9c4fb2cf106c4e3acce5605d5a9a4179c1eddf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0412307fde17a5db36baf1ad1d2b2792d72fa90b3e4a45c8035ddc2d882f8b`  
		Last Modified: Tue, 01 Mar 2022 10:16:30 GMT  
		Size: 117.2 MB (117184912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.17.0-69.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:713ebf05b46b0285e92044ef34022a6cd5bd0191baf4f9bf70537b995a846c3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195295058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d0c08ded51d40c0c24e0ebf77dc949d48f5e3eb670c15b784bd9472c073e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791e7c6030ac15126eefe586e9095bd5b6b0e7ae2f1808b6dda90eab66c9575e`  
		Last Modified: Tue, 01 Mar 2022 11:00:42 GMT  
		Size: 118.7 MB (118686392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:cb559423dd7d079644b2f4ae1842caae74dca530ae2e4e0e8abdf1dfd84faf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:b6dc24d2c05f7d7cdf0fcef7623da367f80d969349a3bca84f1bcdaebe91a9a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276439933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236574319f693fcea39779860b3703709e1fe3b29632860ced1649ca8b27081a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4b760d756a522da3e617513717044b6a609d151ac78e1092690ab7c617a7d3`  
		Last Modified: Tue, 01 Mar 2022 06:49:33 GMT  
		Size: 197.9 MB (197860746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:ab9b65cd0a23e10a0081cdd610804dc2417602f9bcbbb72d89949613e45c5ef0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186002276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ac4c840f6887445c83649eed9c4fb2cf106c4e3acce5605d5a9a4179c1eddf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0412307fde17a5db36baf1ad1d2b2792d72fa90b3e4a45c8035ddc2d882f8b`  
		Last Modified: Tue, 01 Mar 2022 10:16:30 GMT  
		Size: 117.2 MB (117184912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:713ebf05b46b0285e92044ef34022a6cd5bd0191baf4f9bf70537b995a846c3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195295058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d0c08ded51d40c0c24e0ebf77dc949d48f5e3eb670c15b784bd9472c073e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791e7c6030ac15126eefe586e9095bd5b6b0e7ae2f1808b6dda90eab66c9575e`  
		Last Modified: Tue, 01 Mar 2022 11:00:42 GMT  
		Size: 118.7 MB (118686392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:cb559423dd7d079644b2f4ae1842caae74dca530ae2e4e0e8abdf1dfd84faf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b6dc24d2c05f7d7cdf0fcef7623da367f80d969349a3bca84f1bcdaebe91a9a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276439933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236574319f693fcea39779860b3703709e1fe3b29632860ced1649ca8b27081a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4b760d756a522da3e617513717044b6a609d151ac78e1092690ab7c617a7d3`  
		Last Modified: Tue, 01 Mar 2022 06:49:33 GMT  
		Size: 197.9 MB (197860746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:ab9b65cd0a23e10a0081cdd610804dc2417602f9bcbbb72d89949613e45c5ef0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186002276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ac4c840f6887445c83649eed9c4fb2cf106c4e3acce5605d5a9a4179c1eddf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0412307fde17a5db36baf1ad1d2b2792d72fa90b3e4a45c8035ddc2d882f8b`  
		Last Modified: Tue, 01 Mar 2022 10:16:30 GMT  
		Size: 117.2 MB (117184912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:713ebf05b46b0285e92044ef34022a6cd5bd0191baf4f9bf70537b995a846c3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195295058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d0c08ded51d40c0c24e0ebf77dc949d48f5e3eb670c15b784bd9472c073e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=5896bc9fd8543b419870ced8b504b8f33b16c0a0bcf566f3e419e3b35db21006;             SDK_ARCH="x64";;         armhf)             DART_SHA256=56da37cea8b4bc70b17cf08e1b582dcd35392c3611140cda04dcba34bdd4b2ba;             SDK_ARCH="arm";;         arm64)             DART_SHA256=ff5ab6b960a5511eef506236ff5e4b4d115f2786393b59d615c3a0fc242b0639;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-69.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791e7c6030ac15126eefe586e9095bd5b6b0e7ae2f1808b6dda90eab66c9575e`  
		Last Modified: Tue, 01 Mar 2022 11:00:42 GMT  
		Size: 118.7 MB (118686392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:bc3c01156859d85e2e343d9bb87cf57a193dc709d8c9adecdcf71df0b0728704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:7c9216dd7d7941bdcca30a1e800b821894975a86e12c67c28a1e3b1989241d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279599415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966378310e8018866671cdeee1149e820d022abf972eccd357a66c2572c9a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b98a0af9ec88db1c6cfc7ae0f2abd20871aa1f0c667cc9ff13906f2e26d27d`  
		Last Modified: Tue, 01 Mar 2022 06:48:27 GMT  
		Size: 201.0 MB (201020228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:27562f177904bb9c3168ef2c05e761f9253a2c680c1a7a182fb9bd7a7aed8026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187003363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c21651f2a5da4694eefd119768e6db134f1f5ff13ca63c3e3e1e5665f325b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a6a6f6e6609c4abad1d4eb06bd2d4478ab5751d588434f94eaa420cd39d93`  
		Last Modified: Tue, 01 Mar 2022 10:14:30 GMT  
		Size: 118.2 MB (118185999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d318eb926d57fba2dff37583ed20753c4bc63dff132fb8e19f17fe70e31e12b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e33d608bb95be43cd6802ea19fd735d1fd9a5bfc814a2d0ab18f48f02acaa7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a15e3b36348a88307d515493428151bc89ed71317d490a58b0fdda9260be91`  
		Last Modified: Tue, 01 Mar 2022 10:59:47 GMT  
		Size: 119.7 MB (119699694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:bc3c01156859d85e2e343d9bb87cf57a193dc709d8c9adecdcf71df0b0728704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:7c9216dd7d7941bdcca30a1e800b821894975a86e12c67c28a1e3b1989241d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279599415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966378310e8018866671cdeee1149e820d022abf972eccd357a66c2572c9a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b98a0af9ec88db1c6cfc7ae0f2abd20871aa1f0c667cc9ff13906f2e26d27d`  
		Last Modified: Tue, 01 Mar 2022 06:48:27 GMT  
		Size: 201.0 MB (201020228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:27562f177904bb9c3168ef2c05e761f9253a2c680c1a7a182fb9bd7a7aed8026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187003363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c21651f2a5da4694eefd119768e6db134f1f5ff13ca63c3e3e1e5665f325b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a6a6f6e6609c4abad1d4eb06bd2d4478ab5751d588434f94eaa420cd39d93`  
		Last Modified: Tue, 01 Mar 2022 10:14:30 GMT  
		Size: 118.2 MB (118185999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d318eb926d57fba2dff37583ed20753c4bc63dff132fb8e19f17fe70e31e12b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e33d608bb95be43cd6802ea19fd735d1fd9a5bfc814a2d0ab18f48f02acaa7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a15e3b36348a88307d515493428151bc89ed71317d490a58b0fdda9260be91`  
		Last Modified: Tue, 01 Mar 2022 10:59:47 GMT  
		Size: 119.7 MB (119699694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:bc3c01156859d85e2e343d9bb87cf57a193dc709d8c9adecdcf71df0b0728704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:7c9216dd7d7941bdcca30a1e800b821894975a86e12c67c28a1e3b1989241d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279599415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966378310e8018866671cdeee1149e820d022abf972eccd357a66c2572c9a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b98a0af9ec88db1c6cfc7ae0f2abd20871aa1f0c667cc9ff13906f2e26d27d`  
		Last Modified: Tue, 01 Mar 2022 06:48:27 GMT  
		Size: 201.0 MB (201020228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:27562f177904bb9c3168ef2c05e761f9253a2c680c1a7a182fb9bd7a7aed8026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187003363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c21651f2a5da4694eefd119768e6db134f1f5ff13ca63c3e3e1e5665f325b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a6a6f6e6609c4abad1d4eb06bd2d4478ab5751d588434f94eaa420cd39d93`  
		Last Modified: Tue, 01 Mar 2022 10:14:30 GMT  
		Size: 118.2 MB (118185999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d318eb926d57fba2dff37583ed20753c4bc63dff132fb8e19f17fe70e31e12b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e33d608bb95be43cd6802ea19fd735d1fd9a5bfc814a2d0ab18f48f02acaa7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a15e3b36348a88307d515493428151bc89ed71317d490a58b0fdda9260be91`  
		Last Modified: Tue, 01 Mar 2022 10:59:47 GMT  
		Size: 119.7 MB (119699694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:bc3c01156859d85e2e343d9bb87cf57a193dc709d8c9adecdcf71df0b0728704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7c9216dd7d7941bdcca30a1e800b821894975a86e12c67c28a1e3b1989241d54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279599415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966378310e8018866671cdeee1149e820d022abf972eccd357a66c2572c9a25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:46:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:46:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 06:46:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 06:46:46 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 06:46:46 GMT
WORKDIR /root
# Tue, 01 Mar 2022 06:47:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed648f8ba452209b7d9a44ca13e17bebbea5f3e2560dd70a673c7e438b541f`  
		Last Modified: Tue, 01 Mar 2022 06:48:01 GMT  
		Size: 45.1 MB (45073567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb7dff545b6a6e052074de897e0687dc01cd764d96a04f1ebcaea3fde2e45d`  
		Last Modified: Tue, 01 Mar 2022 06:47:51 GMT  
		Size: 2.1 MB (2139224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b98a0af9ec88db1c6cfc7ae0f2abd20871aa1f0c667cc9ff13906f2e26d27d`  
		Last Modified: Tue, 01 Mar 2022 06:48:27 GMT  
		Size: 201.0 MB (201020228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:27562f177904bb9c3168ef2c05e761f9253a2c680c1a7a182fb9bd7a7aed8026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187003363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c21651f2a5da4694eefd119768e6db134f1f5ff13ca63c3e3e1e5665f325b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:10:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:10:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:10:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:10:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:10:55 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:11:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db08f03830a1b9ffb5b514c5233d92c6eaf9d1732cc489f5c5ecb9ba81d6a61f`  
		Last Modified: Tue, 01 Mar 2022 10:13:38 GMT  
		Size: 41.0 MB (40964374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b2da54c316d47333578c6a5427f2e046d4d4c18a7f1e3c6f7ae72e11ac87a`  
		Last Modified: Tue, 01 Mar 2022 10:13:14 GMT  
		Size: 1.3 MB (1287885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0a6a6f6e6609c4abad1d4eb06bd2d4478ab5751d588434f94eaa420cd39d93`  
		Last Modified: Tue, 01 Mar 2022 10:14:30 GMT  
		Size: 118.2 MB (118185999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d318eb926d57fba2dff37583ed20753c4bc63dff132fb8e19f17fe70e31e12b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e33d608bb95be43cd6802ea19fd735d1fd9a5bfc814a2d0ab18f48f02acaa7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:58:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:58:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 01 Mar 2022 10:58:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 01 Mar 2022 10:58:29 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:58:30 GMT
WORKDIR /root
# Tue, 01 Mar 2022 10:58:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3cc63a0c21500bc5eb9671733843dcc20040b39fdc02f35defcf7af59f88d459;             SDK_ARCH="x64";;         armhf)             DART_SHA256=16e0143716b3ad956fcec78bdb15834bcd67619e61ced0a7806328e9d385b2b3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=de9d1c528367f83bbd192bd565af5b7d9d48f76f79baa4c0e4cf64723e3fb8be;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.16.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12adfb02acb2fcd2bfa98e15d99fc8cd292bc11b0fd5e3707a3be9a204863579`  
		Last Modified: Tue, 01 Mar 2022 10:59:36 GMT  
		Size: 45.0 MB (44995126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351b60c321c0c3f56441643c86cd67ed4b8d4bf60a873dbea60d26073aa0e8d`  
		Last Modified: Tue, 01 Mar 2022 10:59:30 GMT  
		Size: 1.6 MB (1556532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a15e3b36348a88307d515493428151bc89ed71317d490a58b0fdda9260be91`  
		Last Modified: Tue, 01 Mar 2022 10:59:47 GMT  
		Size: 119.7 MB (119699694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
