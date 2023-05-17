## `dart:stable-sdk`

```console
$ docker pull dart@sha256:3680873667db3de04d5b54250c9f15da722b27296fcd14013b331412095e32e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:2ebba7fda4dc6f414f9874884c1a7ff9c1e87e88767d365de9547d1d3baa979b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296597515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f935303716ecdbae14d1135328918ffad9a6490af7dc10606f419f966fb49fe7`
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
# Wed, 17 May 2023 20:21:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=caab438213bffba5ab704d88155710327f0fc4326594224714271bf823dfdc70;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a36b77fc9eac1b95ca005d262f81af56c359065b18f25d4a4744249772481c4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d05d9052fe8eba57d4838cea5a29577a34988d882ea9610096f137f256409d03;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dac6f5811643ef5e4811ccf2f7e5c9b0746913cbf896b3b8c53072639dc5b4d2`  
		Last Modified: Wed, 17 May 2023 20:22:08 GMT  
		Size: 217.9 MB (217930576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8954bfe3902a3b7a3b0e4dd27eb185a66c67c9fa9f9478a5e9048624a87cbfe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191265190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd2ef390172353c86a46c41553cc457877e891d9c421e582314fc99440b8e96`
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
# Wed, 17 May 2023 20:57:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=caab438213bffba5ab704d88155710327f0fc4326594224714271bf823dfdc70;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a36b77fc9eac1b95ca005d262f81af56c359065b18f25d4a4744249772481c4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d05d9052fe8eba57d4838cea5a29577a34988d882ea9610096f137f256409d03;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:3765998bbd8667501d82bcec886e2a7ce36c2b9b51b8d5ee695241a1c1e4339b`  
		Last Modified: Wed, 17 May 2023 20:57:58 GMT  
		Size: 122.4 MB (122424385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:995d74fec6d901dbbddbaf5776b79a5ad33ec08d4b5c769fd6254f94d2790eba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200445013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905a5dfcabc66c4d0486608d72b69cd2414cb7afff01f55100fe4e7f0b9c59ed`
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
# Wed, 17 May 2023 20:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=caab438213bffba5ab704d88155710327f0fc4326594224714271bf823dfdc70;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a36b77fc9eac1b95ca005d262f81af56c359065b18f25d4a4744249772481c4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d05d9052fe8eba57d4838cea5a29577a34988d882ea9610096f137f256409d03;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:74e59090b84efc5a17ef4d9ea24fe045ecd0cb65eb9cd793c555aea871bdd87e`  
		Last Modified: Wed, 17 May 2023 20:41:10 GMT  
		Size: 123.8 MB (123820255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
