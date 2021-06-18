## `rust:1-alpine`

```console
$ docker pull rust@sha256:2624c73d2bfe964073ec8153382def5a42ae9ee34ca8c81a25a4e50b0569ea6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:17c40510db4c8eb5b80f8543f10bac3676e4e2e5e3dcf091ce04952c53e987f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258407826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1178cc15e653de052bdd29e5114d0e009ed8e0902eb2f3cb58309f069c5f6a22`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:49:01 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 17 Jun 2021 23:25:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.53.0
# Thu, 17 Jun 2021 23:25:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0be8eca5527a01ceab7f038cf1613c804e74597a07cde2e89d3c7bb2bc3d952`  
		Last Modified: Thu, 15 Apr 2021 02:52:05 GMT  
		Size: 42.2 MB (42173846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c22c6ce94671cbed201daa9a5b2041d8af4105ae5fab8f026f39b827c404749`  
		Last Modified: Thu, 17 Jun 2021 23:30:50 GMT  
		Size: 213.4 MB (213422011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c6f6045225c3ccc0036c2ff8bb196fe6eff45cc60e3924715bec4068b78a3f70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230029190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c27f344dbc9ff554935215d09e47d04170f26376a0e0b6933f6f89f68fd759c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:21:03 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Wed, 16 Jun 2021 11:21:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Wed, 16 Jun 2021 11:21:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='92e38262ebb9440fbdd229618eb85489d2c3d4a74c68b9ef0fdaf200e19521f8' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='4da6988d6bc80de3fa2d239f7de44152c87c257d208562ad9da17065cc08289b' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf5d547724a45171e866f60811b4c2ded56309e2c9f5947606b0bafe3605bed`  
		Last Modified: Wed, 16 Jun 2021 11:24:00 GMT  
		Size: 35.9 MB (35922450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01a4880d2e1b2ac7a19639d32c1758e4b83e0207c105a95683cf769b9938f4f`  
		Last Modified: Wed, 16 Jun 2021 11:24:20 GMT  
		Size: 191.4 MB (191394714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
