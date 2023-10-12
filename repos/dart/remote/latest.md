## `dart:latest`

```console
$ docker pull dart@sha256:b42328ca91e961fdec1346e930df42fb027d51cfba04af2a748764bbc867e1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:167f3b7a768d37c813a953faf72b82c6f2ccbca1e753a960371d413088139b78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296148926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0033636b7f808df29a950bc00984ace57d845ebe46ef5a51f250c25eae9a29`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:35:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:35:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 22:35:04 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 22:35:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:35:04 GMT
WORKDIR /root
# Wed, 11 Oct 2023 22:35:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45c0bb5fb66e490a1f05f4cd349d80465ae33ca359c4fb68dd1c74e658176ca`  
		Last Modified: Wed, 11 Oct 2023 22:36:10 GMT  
		Size: 54.6 MB (54639187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecb3d09a7f21147b48a35dce85aae05f8811cd31156fc58a275aec435712e16`  
		Last Modified: Wed, 11 Oct 2023 22:36:02 GMT  
		Size: 1.8 MB (1800644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de411aff59341d6595bab5539c27772abfccd06ff52dc714d5d7fbe46570febc`  
		Last Modified: Wed, 11 Oct 2023 22:36:30 GMT  
		Size: 210.6 MB (210559221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6449f0231e2683787bdd35de0355f03e88273dfdfafb867f6fcabad05dc3067c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197989816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8ddc7edd0c4939dc05f3c1e378c67967b3ba0307bb57e7cd6bdfe7e00b31b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:13 GMT
ADD file:ec1a6e0aedd76c8fdc8544775f8b553f58950e9435f5cfe919f39374e222cfbb in / 
# Wed, 20 Sep 2023 02:44:14 GMT
CMD ["bash"]
# Thu, 28 Sep 2023 19:39:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 28 Sep 2023 19:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 28 Sep 2023 19:39:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 28 Sep 2023 19:39:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 19:39:38 GMT
WORKDIR /root
# Thu, 28 Sep 2023 19:39:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e886f0f47ef56fcadb6ecaf2116056bbdb273e0afe07ed034498b198d386c04e`  
		Last Modified: Wed, 20 Sep 2023 02:47:36 GMT  
		Size: 29.2 MB (29157221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2537385569e5e48f9f6f3bd4a3974bd39853a1b3f750237ebf646c83dd546b`  
		Last Modified: Thu, 28 Sep 2023 19:41:33 GMT  
		Size: 54.3 MB (54290946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b19c9300ae59e9cb15533b23627fcb5e0bf306d08657eedd25cbccf607ee3d`  
		Last Modified: Thu, 28 Sep 2023 19:41:37 GMT  
		Size: 1.5 MB (1494135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8b93d302fa45056cbe56027d7d43a25d42033495a0deb9ff0e2091643472f0`  
		Last Modified: Thu, 28 Sep 2023 19:42:25 GMT  
		Size: 113.0 MB (113047514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
