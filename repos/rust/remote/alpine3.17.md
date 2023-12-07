## `rust:alpine3.17`

```console
$ docker pull rust@sha256:d45bc42990950fff3a37c0e7e4bc558b2b1fba0b15a2d6677ce9320e7958e886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:alpine3.17` - linux; amd64

```console
$ docker pull rust@sha256:4a201d2a1d3098daea1bedace3698e1af2af152a82765235bdb6e7be72ce0e90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275717536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80f5a74c591a76ac41c57a33764c4166700670ca7434dfdc43f64e7060a6d47`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:50:03 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 07 Dec 2023 19:23:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.74.1
# Thu, 07 Dec 2023 19:24:08 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef39ec453e72776182dce80d9f9e5759c11379a8f8e5263d99e1db99fe5534b`  
		Last Modified: Fri, 01 Dec 2023 07:51:36 GMT  
		Size: 53.1 MB (53089474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c479c33fae42f1a7b9aa29156a4bd973bfbd670ea35fc0c6a14e89df8ca81c`  
		Last Modified: Thu, 07 Dec 2023 19:29:50 GMT  
		Size: 219.2 MB (219248739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:alpine3.17` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:71c055bc48f567cb92cbd8cb2b875a0436ad4776db000cd7a5de045357db899a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279646480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb022fdaf8544d76f01058301627f6d9efc6e4b27700099089e3cb42f6f63c51`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:08:41 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 07 Dec 2023 19:54:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.74.1
# Thu, 07 Dec 2023 19:54:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc66c6dc5162689beac383c8b181a4b127f468783894d6c7172e20fe15123d01`  
		Last Modified: Fri, 01 Dec 2023 09:10:05 GMT  
		Size: 45.6 MB (45608867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a8be9147094a13e7fdaf0f54428261d6875f6ec490c96e6e9647290beac281`  
		Last Modified: Thu, 07 Dec 2023 20:00:16 GMT  
		Size: 230.8 MB (230779265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
