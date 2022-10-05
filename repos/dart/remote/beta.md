## `dart:beta`

```console
$ docker pull dart@sha256:ae24f32a2299a256e04b28b771b627683206f62708e4e30fd1d7b6d8e9f6f8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:8a863e1c35e6b872caeaa323477ac2352254a50494900776360c9513579a3c7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273621420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ea6b0e6d3a07e1540ed0ed4669ceb3164abcb0359104d4f688a58acecd00c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:57:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:57:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Sep 2022 03:57:10 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Sep 2022 03:57:10 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 03:57:10 GMT
WORKDIR /root
# Fri, 23 Sep 2022 19:19:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f6188d09d91bf2759f5447246505d7096159c52eca6b59342752f2e015178298;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ddee1ac517edb839cd6d3a548409672cdcd616ab0897150811a1b842639ab772;             SDK_ARCH="arm";;         arm64)             DART_SHA256=92955b5769f5aad5334a219e8daa6d323c8ae915bbd36435d835f23af0d9c8e0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-146.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d63b6474cd1858e80830a661cd94266316317015c29b48065f8ca8f4be032b2`  
		Last Modified: Tue, 13 Sep 2022 03:57:52 GMT  
		Size: 45.1 MB (45076266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b3e6f150bf6765ed0be2d60b823b718ea7bd975a53d61d41868af1dc4ac11e`  
		Last Modified: Tue, 13 Sep 2022 03:57:45 GMT  
		Size: 2.2 MB (2161955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59ffb4d89a017d7228f38ac5c87ed25b145fd4fde5e82e45f2ef5c750290e6a`  
		Last Modified: Fri, 23 Sep 2022 19:20:41 GMT  
		Size: 195.0 MB (194979078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:b9a77c3399710e0ae67f7346d030a5df4859fc433715e0e43cf5aa99119f3404
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181583332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c411e3163c832afee902faa995319742f8f6d9c136d30096d262f02129ff05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:07:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:07:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 05 Oct 2022 01:07:02 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Oct 2022 01:07:02 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:07:03 GMT
WORKDIR /root
# Wed, 05 Oct 2022 01:07:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f6188d09d91bf2759f5447246505d7096159c52eca6b59342752f2e015178298;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ddee1ac517edb839cd6d3a548409672cdcd616ab0897150811a1b842639ab772;             SDK_ARCH="arm";;         arm64)             DART_SHA256=92955b5769f5aad5334a219e8daa6d323c8ae915bbd36435d835f23af0d9c8e0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-146.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee2ba6dbb90fca59a02490ded2c70ae39d2370c99af2878d715cfe32456dc99`  
		Last Modified: Wed, 05 Oct 2022 01:08:34 GMT  
		Size: 41.0 MB (40956155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71f3a922ad3f4e673ec9d2b89cefc49bab9db492c408e780485e4d32f67de04`  
		Last Modified: Wed, 05 Oct 2022 01:08:22 GMT  
		Size: 1.3 MB (1288534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48a13eb73106e9915482a10324b8780c4e76c57f86b5a36d8a4c4c7a1e14891`  
		Last Modified: Wed, 05 Oct 2022 01:09:52 GMT  
		Size: 112.8 MB (112759444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:e6a9277eb6397fb7664411739744ae7101709fb57d1490509fd1869babdabe2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190346770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34f871603bc921957564ea119fed7d3b9122fefacf6f27a98924d987a049b0b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:22:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:22:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 05 Oct 2022 01:22:53 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Oct 2022 01:22:54 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:22:55 GMT
WORKDIR /root
# Wed, 05 Oct 2022 01:23:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f6188d09d91bf2759f5447246505d7096159c52eca6b59342752f2e015178298;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ddee1ac517edb839cd6d3a548409672cdcd616ab0897150811a1b842639ab772;             SDK_ARCH="arm";;         arm64)             DART_SHA256=92955b5769f5aad5334a219e8daa6d323c8ae915bbd36435d835f23af0d9c8e0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.19.0-146.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851b1e9bf245b4ed8d0d5804b0b80ccf0d21d77250ae8bdaa46249bf97870964`  
		Last Modified: Wed, 05 Oct 2022 01:24:03 GMT  
		Size: 44.8 MB (44791748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0266f3bb3cdeeb4fd1780909e2397c47d92bd68d7678de447c55f13da54b62ea`  
		Last Modified: Wed, 05 Oct 2022 01:23:56 GMT  
		Size: 1.6 MB (1556382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699dadf2353c260be1cc2d2832d8cb9de37f2e7d15375eeb74bd20d663c51b3a`  
		Last Modified: Wed, 05 Oct 2022 01:25:04 GMT  
		Size: 113.9 MB (113934245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
