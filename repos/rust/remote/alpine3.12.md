## `rust:alpine3.12`

```console
$ docker pull rust@sha256:b385ed6aea843542dec952048bee48be581d7ba35e283d294459c256036012d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:alpine3.12` - linux; amd64

```console
$ docker pull rust@sha256:1805537f93a206f131e23eada2a9fc0da67e5ac88ac57cd4e38f4273bc32e58f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239638881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb2639aeaf946d1655db34f3e026b4be402c48265d71a64fc34527874dcb2ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 09:47:40 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Fri, 26 Mar 2021 09:47:40 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.51.0
# Fri, 26 Mar 2021 09:47:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='05c5c05ec76671d73645aac3afbccf2187352fce7e46fc85be859f52a42797f6' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='6a8a480d8d9e7f8c6979d7f8b12bc59da13db67970f7b13161ff409f0a771213' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c531bfa78e8e7b16fffffc37b8af78f66949e4171ec56f5d50672a437d95d88`  
		Last Modified: Fri, 26 Mar 2021 09:50:47 GMT  
		Size: 47.6 MB (47613548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbd5ecccc8a3030d8e0293ce2170209f32e945a3c5836155fa0eb1b876a55fc`  
		Last Modified: Fri, 26 Mar 2021 09:51:08 GMT  
		Size: 189.2 MB (189225571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:909dd3290973dd880bba1d741e27182bd9e7d9c1e6d9eb29de8b4c98e1eeb636
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228489609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d5d738b24f5588774a9ca8e65ec3ed5e4f95963471692df2c25c15776b11eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 12:35:38 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Fri, 26 Mar 2021 12:35:40 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.51.0
# Fri, 26 Mar 2021 12:36:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='05c5c05ec76671d73645aac3afbccf2187352fce7e46fc85be859f52a42797f6' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='6a8a480d8d9e7f8c6979d7f8b12bc59da13db67970f7b13161ff409f0a771213' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.23.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7f365e1f152a3e6eb15c8766f1600caf466abb8a54e1a35a2e6fcaafe2d6db`  
		Last Modified: Fri, 26 Mar 2021 12:39:58 GMT  
		Size: 38.6 MB (38561471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184f745e0c752d0d0927708f7365df20e7ff34daafc899f150a00beae0c28983`  
		Last Modified: Fri, 26 Mar 2021 12:40:34 GMT  
		Size: 187.2 MB (187218446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
