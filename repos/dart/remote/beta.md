## `dart:beta`

```console
$ docker pull dart@sha256:2b7d569e8f17c5d41d80dc1bda1e2f03c4189a556f470c17fd6e204744c2acc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:3e96bb61088639d6d8ceb2158cfae8d979ffe0502092c071b178175b4ddbb227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297269091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0aa9b4b68f8c9e6026e33f6b799e6da20f466f107d7973eb11b0a4e182043e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:02:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:02:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 23 May 2023 02:02:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 23 May 2023 02:02:39 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:02:40 GMT
WORKDIR /root
# Tue, 23 May 2023 02:03:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1edcf9e1c5be94633fa025614866d49c437322ab3cc759822645287ddb9bfd62;             SDK_ARCH="x64";;         armhf)             DART_SHA256=82c73e025efa6c4020985f85fe2b46264000295a402e1be9e787f54c17eb2590;             SDK_ARCH="arm";;         arm64)             DART_SHA256=63442bd94a4bcb043fccf9f3f22a5ca846fbb3a3933eea84dcfe8502f8f767de;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.1.0-63.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3572b44d335a64cd955d4b4f239be22f270eae3cb4aca267178184673f806503`  
		Last Modified: Tue, 23 May 2023 02:03:34 GMT  
		Size: 45.1 MB (45102949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c8976d47ff0430694019e0a77b46eb92804bfcc3a2d3ac81ea6971476f3127`  
		Last Modified: Tue, 23 May 2023 02:03:28 GMT  
		Size: 2.2 MB (2160696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017ed06ffd303ab8d53d1db147213878637053f777eb8653753bcc2631c51f7f`  
		Last Modified: Tue, 23 May 2023 02:04:46 GMT  
		Size: 218.6 MB (218601860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:772862ed0c40e86dec7fc1f75a437f8d29509833c152fa36a564f2811d177b71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191523970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0f55150b2d20b6da2dd3fa5cfc55723cf6f6873237a97a4d068f0338bb0039`
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
# Wed, 10 May 2023 16:57:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1edcf9e1c5be94633fa025614866d49c437322ab3cc759822645287ddb9bfd62;             SDK_ARCH="x64";;         armhf)             DART_SHA256=82c73e025efa6c4020985f85fe2b46264000295a402e1be9e787f54c17eb2590;             SDK_ARCH="arm";;         arm64)             DART_SHA256=63442bd94a4bcb043fccf9f3f22a5ca846fbb3a3933eea84dcfe8502f8f767de;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.1.0-63.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:7b76f5ede009e5ee4f3be443e741613f889944e729f16928ad2709b9d9b0c028`  
		Last Modified: Wed, 10 May 2023 16:58:59 GMT  
		Size: 122.7 MB (122683165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4a2d4689caaf73bd66fc8f815e9608d98d52c77c0f633e8a7451b951e4ad7fdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200705129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436ad7cf4ae165cce24cc1dc9f6b7f1f2c31e4d1323b7c487a9448faaf57cb77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:43:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:43:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 23 May 2023 01:43:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 23 May 2023 01:43:44 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 01:43:44 GMT
WORKDIR /root
# Tue, 23 May 2023 01:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1edcf9e1c5be94633fa025614866d49c437322ab3cc759822645287ddb9bfd62;             SDK_ARCH="x64";;         armhf)             DART_SHA256=82c73e025efa6c4020985f85fe2b46264000295a402e1be9e787f54c17eb2590;             SDK_ARCH="arm";;         arm64)             DART_SHA256=63442bd94a4bcb043fccf9f3f22a5ca846fbb3a3933eea84dcfe8502f8f767de;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.1.0-63.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9834f1e82c8c7a78091fc1d2da8d589129c39bb91a9f424bcca2633901f7d3fe`  
		Last Modified: Tue, 23 May 2023 01:44:25 GMT  
		Size: 45.0 MB (45011120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc4b42a8d93958e89deb953ea286363c4541e1c65e8ea0f3ed34c177a7163b8`  
		Last Modified: Tue, 23 May 2023 01:44:21 GMT  
		Size: 1.6 MB (1560879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3fff2216e0d2bfb5c1cf9eaa5494ed646c21921dae1b88da22c00dff67af15`  
		Last Modified: Tue, 23 May 2023 01:45:07 GMT  
		Size: 124.1 MB (124080383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
