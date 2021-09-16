<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:2`](#dart2)
-	[`dart:2-sdk`](#dart2-sdk)
-	[`dart:2.14`](#dart214)
-	[`dart:2.14-sdk`](#dart214-sdk)
-	[`dart:2.14.2`](#dart2142)
-	[`dart:2.14.2-sdk`](#dart2142-sdk)
-	[`dart:2.15.0-82.2.beta`](#dart2150-822beta)
-	[`dart:2.15.0-82.2.beta-sdk`](#dart2150-822beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:2`

```console
$ docker pull dart@sha256:ce77cc9081a3986a633b6047dc4b1a42c89841520cea5edbb6ddd84ad52b2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:2` - linux; amd64

```console
$ docker pull dart@sha256:3faaba5f47cfd9b1c35269673d358b07f9295763afef1efecf7aa5d01f35b266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289038863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b82d3b82f963dc2ae8b51c9f326e24ec0a2b5d7b86ddef5c6869c833a90839f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:12 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "bd352ab4df3de74f837dcc95f86917d925d71793c4b26c2650e0cf814c6e22bf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b631065564c5562b428efa032e71289caa8a8153788a2343fd248eb3d49e8`  
		Last Modified: Thu, 16 Sep 2021 19:22:21 GMT  
		Size: 210.0 MB (209950687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2-sdk`

```console
$ docker pull dart@sha256:ce77cc9081a3986a633b6047dc4b1a42c89841520cea5edbb6ddd84ad52b2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:3faaba5f47cfd9b1c35269673d358b07f9295763afef1efecf7aa5d01f35b266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289038863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b82d3b82f963dc2ae8b51c9f326e24ec0a2b5d7b86ddef5c6869c833a90839f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:12 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "bd352ab4df3de74f837dcc95f86917d925d71793c4b26c2650e0cf814c6e22bf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b631065564c5562b428efa032e71289caa8a8153788a2343fd248eb3d49e8`  
		Last Modified: Thu, 16 Sep 2021 19:22:21 GMT  
		Size: 210.0 MB (209950687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.14`

```console
$ docker pull dart@sha256:ce77cc9081a3986a633b6047dc4b1a42c89841520cea5edbb6ddd84ad52b2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:2.14` - linux; amd64

```console
$ docker pull dart@sha256:3faaba5f47cfd9b1c35269673d358b07f9295763afef1efecf7aa5d01f35b266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289038863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b82d3b82f963dc2ae8b51c9f326e24ec0a2b5d7b86ddef5c6869c833a90839f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:12 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "bd352ab4df3de74f837dcc95f86917d925d71793c4b26c2650e0cf814c6e22bf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b631065564c5562b428efa032e71289caa8a8153788a2343fd248eb3d49e8`  
		Last Modified: Thu, 16 Sep 2021 19:22:21 GMT  
		Size: 210.0 MB (209950687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.14-sdk`

```console
$ docker pull dart@sha256:ce77cc9081a3986a633b6047dc4b1a42c89841520cea5edbb6ddd84ad52b2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:2.14-sdk` - linux; amd64

```console
$ docker pull dart@sha256:3faaba5f47cfd9b1c35269673d358b07f9295763afef1efecf7aa5d01f35b266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289038863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b82d3b82f963dc2ae8b51c9f326e24ec0a2b5d7b86ddef5c6869c833a90839f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:12 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "bd352ab4df3de74f837dcc95f86917d925d71793c4b26c2650e0cf814c6e22bf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b631065564c5562b428efa032e71289caa8a8153788a2343fd248eb3d49e8`  
		Last Modified: Thu, 16 Sep 2021 19:22:21 GMT  
		Size: 210.0 MB (209950687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.14.2`

```console
$ docker pull dart@sha256:ce77cc9081a3986a633b6047dc4b1a42c89841520cea5edbb6ddd84ad52b2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:2.14.2` - linux; amd64

```console
$ docker pull dart@sha256:3faaba5f47cfd9b1c35269673d358b07f9295763afef1efecf7aa5d01f35b266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289038863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b82d3b82f963dc2ae8b51c9f326e24ec0a2b5d7b86ddef5c6869c833a90839f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:12 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "bd352ab4df3de74f837dcc95f86917d925d71793c4b26c2650e0cf814c6e22bf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b631065564c5562b428efa032e71289caa8a8153788a2343fd248eb3d49e8`  
		Last Modified: Thu, 16 Sep 2021 19:22:21 GMT  
		Size: 210.0 MB (209950687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.14.2-sdk`

```console
$ docker pull dart@sha256:ce77cc9081a3986a633b6047dc4b1a42c89841520cea5edbb6ddd84ad52b2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:2.14.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:3faaba5f47cfd9b1c35269673d358b07f9295763afef1efecf7aa5d01f35b266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289038863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b82d3b82f963dc2ae8b51c9f326e24ec0a2b5d7b86ddef5c6869c833a90839f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:12 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "bd352ab4df3de74f837dcc95f86917d925d71793c4b26c2650e0cf814c6e22bf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b631065564c5562b428efa032e71289caa8a8153788a2343fd248eb3d49e8`  
		Last Modified: Thu, 16 Sep 2021 19:22:21 GMT  
		Size: 210.0 MB (209950687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.15.0-82.2.beta`

```console
$ docker pull dart@sha256:5ed907e12f504d4fc4dca243e55aeffb254600f12f6116062a9baf6ab956f582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:2.15.0-82.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:0e1ee6a5fef6f23062986f6ae08f3efbda663371b3cc9ff0bbdae18f5f50251d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280358768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c41b0ec1663c41ac00dfc316c1d27a1399480b42ec795f689819dad674083ad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:30 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.15.0-82.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "3f23b4ca6d7ffeadad21cd69577eabcfb5d872cbd005f04b5d4f58c1866dcf04 *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62b1c6d3666a6e7afce85996cf1a945cf16586f8df4e467ef2009fd4c80abd3`  
		Last Modified: Thu, 16 Sep 2021 19:23:27 GMT  
		Size: 201.3 MB (201270592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.15.0-82.2.beta-sdk`

```console
$ docker pull dart@sha256:5ed907e12f504d4fc4dca243e55aeffb254600f12f6116062a9baf6ab956f582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:2.15.0-82.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:0e1ee6a5fef6f23062986f6ae08f3efbda663371b3cc9ff0bbdae18f5f50251d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280358768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c41b0ec1663c41ac00dfc316c1d27a1399480b42ec795f689819dad674083ad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:30 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.15.0-82.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "3f23b4ca6d7ffeadad21cd69577eabcfb5d872cbd005f04b5d4f58c1866dcf04 *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62b1c6d3666a6e7afce85996cf1a945cf16586f8df4e467ef2009fd4c80abd3`  
		Last Modified: Thu, 16 Sep 2021 19:23:27 GMT  
		Size: 201.3 MB (201270592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:5ed907e12f504d4fc4dca243e55aeffb254600f12f6116062a9baf6ab956f582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:0e1ee6a5fef6f23062986f6ae08f3efbda663371b3cc9ff0bbdae18f5f50251d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280358768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c41b0ec1663c41ac00dfc316c1d27a1399480b42ec795f689819dad674083ad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:30 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.15.0-82.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "3f23b4ca6d7ffeadad21cd69577eabcfb5d872cbd005f04b5d4f58c1866dcf04 *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62b1c6d3666a6e7afce85996cf1a945cf16586f8df4e467ef2009fd4c80abd3`  
		Last Modified: Thu, 16 Sep 2021 19:23:27 GMT  
		Size: 201.3 MB (201270592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:5ed907e12f504d4fc4dca243e55aeffb254600f12f6116062a9baf6ab956f582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:0e1ee6a5fef6f23062986f6ae08f3efbda663371b3cc9ff0bbdae18f5f50251d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280358768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c41b0ec1663c41ac00dfc316c1d27a1399480b42ec795f689819dad674083ad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:30 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.15.0-82.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "3f23b4ca6d7ffeadad21cd69577eabcfb5d872cbd005f04b5d4f58c1866dcf04 *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62b1c6d3666a6e7afce85996cf1a945cf16586f8df4e467ef2009fd4c80abd3`  
		Last Modified: Thu, 16 Sep 2021 19:23:27 GMT  
		Size: 201.3 MB (201270592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:ce77cc9081a3986a633b6047dc4b1a42c89841520cea5edbb6ddd84ad52b2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:3faaba5f47cfd9b1c35269673d358b07f9295763afef1efecf7aa5d01f35b266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289038863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b82d3b82f963dc2ae8b51c9f326e24ec0a2b5d7b86ddef5c6869c833a90839f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:12 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "bd352ab4df3de74f837dcc95f86917d925d71793c4b26c2650e0cf814c6e22bf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b631065564c5562b428efa032e71289caa8a8153788a2343fd248eb3d49e8`  
		Last Modified: Thu, 16 Sep 2021 19:22:21 GMT  
		Size: 210.0 MB (209950687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:ce77cc9081a3986a633b6047dc4b1a42c89841520cea5edbb6ddd84ad52b2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:3faaba5f47cfd9b1c35269673d358b07f9295763afef1efecf7aa5d01f35b266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289038863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b82d3b82f963dc2ae8b51c9f326e24ec0a2b5d7b86ddef5c6869c833a90839f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:12 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "bd352ab4df3de74f837dcc95f86917d925d71793c4b26c2650e0cf814c6e22bf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b631065564c5562b428efa032e71289caa8a8153788a2343fd248eb3d49e8`  
		Last Modified: Thu, 16 Sep 2021 19:22:21 GMT  
		Size: 210.0 MB (209950687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:ce77cc9081a3986a633b6047dc4b1a42c89841520cea5edbb6ddd84ad52b2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:3faaba5f47cfd9b1c35269673d358b07f9295763afef1efecf7aa5d01f35b266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289038863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b82d3b82f963dc2ae8b51c9f326e24ec0a2b5d7b86ddef5c6869c833a90839f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:12 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "bd352ab4df3de74f837dcc95f86917d925d71793c4b26c2650e0cf814c6e22bf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b631065564c5562b428efa032e71289caa8a8153788a2343fd248eb3d49e8`  
		Last Modified: Thu, 16 Sep 2021 19:22:21 GMT  
		Size: 210.0 MB (209950687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:ce77cc9081a3986a633b6047dc4b1a42c89841520cea5edbb6ddd84ad52b2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:3faaba5f47cfd9b1c35269673d358b07f9295763afef1efecf7aa5d01f35b266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289038863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b82d3b82f963dc2ae8b51c9f326e24ec0a2b5d7b86ddef5c6869c833a90839f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:33:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:33:21 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 03 Sep 2021 03:33:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 03 Sep 2021 03:33:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 03:33:21 GMT
WORKDIR /root
# Thu, 16 Sep 2021 19:21:12 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.14.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "bd352ab4df3de74f837dcc95f86917d925d71793c4b26c2650e0cf814c6e22bf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7e1abeaae14b916e75f56944ce7bcfe42a03875edb1bf4377b00df41aae202`  
		Last Modified: Fri, 03 Sep 2021 03:34:26 GMT  
		Size: 49.6 MB (49583194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ba2d113bca583e95fd1ffd40466d29c60c848eb97cae88f7c707a78e107c3a`  
		Last Modified: Fri, 03 Sep 2021 03:34:17 GMT  
		Size: 2.4 MB (2359138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b631065564c5562b428efa032e71289caa8a8153788a2343fd248eb3d49e8`  
		Last Modified: Thu, 16 Sep 2021 19:22:21 GMT  
		Size: 210.0 MB (209950687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
