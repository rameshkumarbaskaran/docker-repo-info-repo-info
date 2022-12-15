## `rust:1-alpine3.17`

```console
$ docker pull rust@sha256:8599c8d0606df8eac2061bd44a63fc25785213a06efac1cda79ef7efd7bdc4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:1-alpine3.17` - linux; amd64

```console
$ docker pull rust@sha256:85c2503eb43caaf02cdcd8e481946e3c97ef2e074336a6f0a06e2b37bb90e4f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.0 MB (272961917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b978714481278d5e789661121b99465cf3b69b723fac8834ee6114d220b110be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Dec 2022 20:22:36 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 15 Dec 2022 20:22:36 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.66.0
# Thu, 15 Dec 2022 20:22:56 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5171e409b9fde385abcc01256c77c9aff1ac94a8318621724675ecd6ed559e6a`  
		Last Modified: Thu, 15 Dec 2022 20:27:26 GMT  
		Size: 53.1 MB (53091066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0debe0b7c52857c948142f56c26a907d9d6f170ec621cbbb00f11edfdc671da`  
		Last Modified: Thu, 15 Dec 2022 20:27:49 GMT  
		Size: 216.5 MB (216500145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:56366791f0ddb1c15955e607f60120a0cbb78c5e6a523fb80bb5b639f33c9794
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258030472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eecbd0d0667bc5ee65f65c9e58ab9f75fc8f685ab9576fa50029fa0974227d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 15 Dec 2022 19:49:19 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 15 Dec 2022 19:49:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.66.0
# Thu, 15 Dec 2022 19:49:32 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47a17aaa7548ed1211281bc6eed0c98037907155c7ac8d8bea43e63c32ecc2e`  
		Last Modified: Thu, 15 Dec 2022 19:53:56 GMT  
		Size: 45.6 MB (45611188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e222af2929cfbd2e522c723ff2697a0b482bde46640bbd40d6493a6262927f`  
		Last Modified: Thu, 15 Dec 2022 19:54:13 GMT  
		Size: 209.2 MB (209160094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
