## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:38e433fedd680ababa25d3fe7a2afe56b20120b04f2f66d97b86b76642054614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:550a8be5c5a7440c499dab04973d02981f8a502df64eff5a76e243ca5924ab1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273651208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04a2b9e6bf0edfd0dafbd2db947e4aa869b22b86e7023d5165a09596d9d230c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:19:49 GMT
ADD file:90a0d468135989831892f177bf4f3f44d0d0b9754439dd04430cf52fae06e7f4 in / 
# Tue, 23 May 2023 01:19:49 GMT
CMD ["bash"]
# Tue, 23 May 2023 15:10:27 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.69.0
# Tue, 23 May 2023 15:11:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:8c1995e9172ea705aef0df96fa13d406aa998774aa999305adc5285ae4ee63f5`  
		Last Modified: Tue, 23 May 2023 01:23:31 GMT  
		Size: 29.1 MB (29096523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d7c1029b6db5efb1b54ac1e58763a88572f28610946db1a71acecb945315e2`  
		Last Modified: Tue, 23 May 2023 15:15:30 GMT  
		Size: 244.6 MB (244554685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:5632fcd7b533e2f50daefe99e66c77963ee5ed83b278feacb041f3b24d2ad1db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283113700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf41ff11d70e4f198ab51212b1544083a0cf38635471f0ec47c47d1fa5341517`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:57:33 GMT
ADD file:037d6e350c9346e6837bf9acd5e5b4df0a9cd021add937ff0771277d7ec7232f in / 
# Tue, 23 May 2023 00:57:34 GMT
CMD ["bash"]
# Fri, 02 Jun 2023 19:16:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.70.0
# Fri, 02 Jun 2023 19:16:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:ee32a6c390ec361a7649b51bf48002039f994aa5c3c6c2efb7fb87300c1fa0ac`  
		Last Modified: Tue, 23 May 2023 01:01:07 GMT  
		Size: 24.8 MB (24785973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b092e2e0eee1f8a776e018adc5db7ae42ac08d1719e5cb6dd1e78e6aa7e9e37`  
		Last Modified: Fri, 02 Jun 2023 19:21:51 GMT  
		Size: 258.3 MB (258327727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fbef2f852591e86cad374e0c7bd52f9e068de4424136073163e10bcbb6b2792b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334410868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4eb16ff4255bf6a44417a8ce3d9d5ef69bc25a382a9572d9a292754ae6abf0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:01 GMT
ADD file:2d1b40afe3cbc1078eaac3d82c5e042d5e5ee3f738022b67fb4d257aca72ad7f in / 
# Tue, 23 May 2023 00:43:02 GMT
CMD ["bash"]
# Tue, 23 May 2023 06:59:16 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.69.0
# Tue, 23 May 2023 06:59:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:a21a5599f6b90192bffa7704c6993b8947d442ef74492f0c7b0884b882bb86ec`  
		Last Modified: Tue, 23 May 2023 00:45:32 GMT  
		Size: 29.1 MB (29134014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1190cdf12b49d53fa8816a0d24e3b67b61c83bbf0887260d6ccbe1376c2b9a45`  
		Last Modified: Tue, 23 May 2023 07:04:35 GMT  
		Size: 305.3 MB (305276854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:06f1872cffa394dd6b92330832dfec97a6a7e176e11b17d2faf4cff6074c6cdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.7 MB (286681127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3e4fd05699137a97672618a969bfae4fea81c3803fe286b8f097bdc3b1ef72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:38:58 GMT
ADD file:f14e9f23053dc86295861792149e7371dd7feaf5f8ca42a3fcb0ced993b8bf19 in / 
# Tue, 23 May 2023 00:38:59 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:46:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.69.0
# Tue, 23 May 2023 01:47:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:d9d3f26c431f5af55b9a486d2ecb62055c5856a1fab5ec40940601863cfcf75d`  
		Last Modified: Tue, 23 May 2023 00:43:43 GMT  
		Size: 30.1 MB (30116808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a38c81efed5c9709c9399e8a91002d00f9d0455fca4bd11a0b2b962058ac30e`  
		Last Modified: Tue, 23 May 2023 01:51:02 GMT  
		Size: 256.6 MB (256564319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
