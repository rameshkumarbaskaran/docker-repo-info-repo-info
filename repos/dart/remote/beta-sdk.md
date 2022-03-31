## `dart:beta-sdk`

```console
$ docker pull dart@sha256:f5398d5b15ae20effd566c224b9d1bb9e05d2b040f03a021291a2755855a0f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5cc036d14ff936b25e32d2bbd49b4a54b6053436a736085dd2b038a3824d3477
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278286837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034594fd456349fe8e42d89c7f10a408c8bcb7c833d5ebf3eb0edc687ee39f11`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:45:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:45:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 29 Mar 2022 17:45:53 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 29 Mar 2022 17:45:53 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:45:54 GMT
WORKDIR /root
# Tue, 29 Mar 2022 17:46:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edca0fe2afb7cb2a5d6c1ebc65cc9cf92db50940cad452de8ff0040272fe4444;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5a6a93f26d38037c5de99f4b6dc6d9b61d30409f6e405e1704db337a4514e8ca;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4bb7866c4fdda23e3d9603b27b3c669376b3740b7b9eca2feb8e9ccbc1673bb8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-182.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45f2555ee8e1d058a6a21c44149f22779e3a9c548f9fead125028706e1ee699`  
		Last Modified: Tue, 29 Mar 2022 17:46:51 GMT  
		Size: 45.1 MB (45072878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14bdf86bbdd984efc950a42c237605d8bc9d6e8cde4b21c8b7297123a345f3e`  
		Last Modified: Tue, 29 Mar 2022 17:46:44 GMT  
		Size: 2.1 MB (2139545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b789dcf7d21381684cf9d7100dd464c5be0105e3ac9484c7e236cb91a126a9ef`  
		Last Modified: Tue, 29 Mar 2022 17:48:09 GMT  
		Size: 199.7 MB (199695957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f223e95a0a59196edfbdeab6f108a5908309e82a48b1c78039e63e3cab7c4397
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186845682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91cb93b2b09c16129202ee7d9d78d37dc650f6d604317ea6fa8ffb034f3da33`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:18:34 GMT
ADD file:e1835d1a0c70a0335757f211893e5d12ddf797e489e10434c0982bdf9b234f67 in / 
# Tue, 29 Mar 2022 02:18:36 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 21:49:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 21:49:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 30 Mar 2022 21:49:42 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 30 Mar 2022 21:49:42 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 21:49:43 GMT
WORKDIR /root
# Wed, 30 Mar 2022 21:50:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c2754bfd46b080c58699ba704ae8212c04ea8e907bec1d9d83d8768adfa587bc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a0575c89e7ceaf1a196929da07951dbc8d5333b2dbde49d456769f55aaaa70ca;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3834827f270d9c1fe285815339991ab7ee5862a6b3c647af933a8206a62a867f;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-182.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:f98812e1a494a683a5b3dea593dd2ef305f5f732193044c147f22e44b00164bc`  
		Last Modified: Tue, 29 Mar 2022 02:34:13 GMT  
		Size: 26.6 MB (26575370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82dffa22f8daa2ba79755d9d7468a2c3a642da5654d231a2a2bf3406ace9914`  
		Last Modified: Wed, 30 Mar 2022 21:52:25 GMT  
		Size: 41.0 MB (40966675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2d8112f6894d4be8f01a13f51bdba197a6f75bba4b585b34ff314a26a21526`  
		Last Modified: Wed, 30 Mar 2022 21:52:01 GMT  
		Size: 1.3 MB (1288084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae82c6d2779a292d9330c8faa02c04f1896d2ba364bb98a47941be03a7f915`  
		Last Modified: Wed, 30 Mar 2022 21:55:19 GMT  
		Size: 118.0 MB (118015553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:67d3b16535b91e0b665df227745624b5186f8ba2324d4639de8b3f23464d9507
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195924730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f155bd28a217931b113dd037428fce12a7adb338c8800a2b317195c76cbd4a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:33:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:33:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 30 Mar 2022 02:33:17 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 30 Mar 2022 02:33:18 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 02:33:19 GMT
WORKDIR /root
# Wed, 30 Mar 2022 02:33:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edca0fe2afb7cb2a5d6c1ebc65cc9cf92db50940cad452de8ff0040272fe4444;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5a6a93f26d38037c5de99f4b6dc6d9b61d30409f6e405e1704db337a4514e8ca;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4bb7866c4fdda23e3d9603b27b3c669376b3740b7b9eca2feb8e9ccbc1673bb8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-182.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a423e5736d56d1e654dc7ea718c973984c74081bc9b6ea10355a237c6b0be05`  
		Last Modified: Wed, 30 Mar 2022 02:34:28 GMT  
		Size: 44.8 MB (44789449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b4a6eab11a627b70631d84ed29f1de4e160d27ed55ae8e732e0c1ff17b1ff`  
		Last Modified: Wed, 30 Mar 2022 02:34:22 GMT  
		Size: 1.6 MB (1556723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14cda60003397106d1cfa25d8dfc37cf475cd7db8cdeeb629bf2dd19cd3a7c2`  
		Last Modified: Wed, 30 Mar 2022 02:35:30 GMT  
		Size: 119.5 MB (119514247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
