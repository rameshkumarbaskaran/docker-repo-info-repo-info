## `rust:1-alpine3.14`

```console
$ docker pull rust@sha256:cef19005da73b5de5fe6f6d25d8d8552c7a386920a684592e3bf5131a61b3ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:1-alpine3.14` - linux; amd64

```console
$ docker pull rust@sha256:8a7f92cf840d15be8ee532ee4aee9e00b94cf13e696c04017e41c0f24ec96676
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.0 MB (284043201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e99bbdf56141c12853b515a0ef0336ed10434bc6937e7441079bffccb6324e0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:53:22 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Sat, 28 Aug 2021 00:53:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.54.0
# Sat, 28 Aug 2021 00:53:51 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ea2bb3df1724da0bb9bbf8d43f7a5b7192610627c590c2fd4b8e0770230cbf`  
		Last Modified: Sat, 28 Aug 2021 00:54:55 GMT  
		Size: 42.4 MB (42351625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3ab885cfec409e9e215f36ebd033b89c6a970da783e9ee89d486e9f98e77d4`  
		Last Modified: Sat, 28 Aug 2021 00:55:25 GMT  
		Size: 238.9 MB (238877130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1e07ee837724e4ee00121360bdf01e09765620149a1da4708f86699cf65fde4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268631291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b244b34acac4cdbcb3afbe63353fe752aed608685f9ef3a911d839bd07172afc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 01:47:26 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Sat, 28 Aug 2021 01:47:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.54.0
# Sat, 28 Aug 2021 01:47:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefe268940ca3d7bb085e849944a03446fcf19da418986a662e594f7b558e670`  
		Last Modified: Sat, 28 Aug 2021 01:49:36 GMT  
		Size: 35.9 MB (35936466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ff408bbc42112e9461b46b590c74386bfec0415f751a0404ebe536f3d0cd1c`  
		Last Modified: Sat, 28 Aug 2021 01:50:05 GMT  
		Size: 230.0 MB (229982998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
