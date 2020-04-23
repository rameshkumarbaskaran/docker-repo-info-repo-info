## `rust:slim-stretch`

```console
$ docker pull rust@sha256:01d9a14e32cce6a4c081d77764176a66c402e969f5212be4810fc54221487f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:slim-stretch` - linux; amd64

```console
$ docker pull rust@sha256:20ddd63eebc07bd3b1e43b165e6c5875c8653bcf1036b36327539110b6a1a975
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190986182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cfaa2537f687900a9c37f3dacbc4238873ff5eea3d104b065dbf550252d1b5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 22:25:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.42.0
# Thu, 16 Apr 2020 22:26:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ad1f8b5199b3b9e231472ed7aa08d2e5d1d539198a15c5b1e53c746aad81d27b' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6c6c3789dabf12171c7f500e06d21d8004b5318a5083df8b0b02c0e5ef1d017b' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='26942c80234bac34b3c1352abbd9187d3e23b43dae3cf56a9f9c1ea8ee53076d' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ae12bc294a34e566579deba3e066245d09b8871dc021ef45fc715dced05297' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.21.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fc8306bf3c7d64f52ad5215b56882d0719e3e24d5896925bf503dc3f0e2c9f`  
		Last Modified: Thu, 16 Apr 2020 22:30:02 GMT  
		Size: 168.5 MB (168472706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:94f92675b4e6974cb35da764ae6ee54733202d786836d9c59035689563bb615d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190381207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7164aec15578ea89d930a9d50342a7fb946432bcf26576014e0227005ed264c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 14:02:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.42.0
# Thu, 23 Apr 2020 14:03:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ad1f8b5199b3b9e231472ed7aa08d2e5d1d539198a15c5b1e53c746aad81d27b' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6c6c3789dabf12171c7f500e06d21d8004b5318a5083df8b0b02c0e5ef1d017b' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='26942c80234bac34b3c1352abbd9187d3e23b43dae3cf56a9f9c1ea8ee53076d' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ae12bc294a34e566579deba3e066245d09b8871dc021ef45fc715dced05297' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.21.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f8539d7cd1ebe3d3eed40c3370985f4a9ba88645ab3d715693326822f61798`  
		Last Modified: Thu, 23 Apr 2020 14:06:56 GMT  
		Size: 171.1 MB (171082744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ce575a2963f21f4548c2cf3e1c4007333b2b569bdc9d31dea80bfa013122bf26
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191009738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac001b8ff9cb69e4b2c8807fb7bba859aafb0a9791121100e6009d2f4af6a90`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 15:55:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.42.0
# Thu, 23 Apr 2020 15:55:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ad1f8b5199b3b9e231472ed7aa08d2e5d1d539198a15c5b1e53c746aad81d27b' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6c6c3789dabf12171c7f500e06d21d8004b5318a5083df8b0b02c0e5ef1d017b' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='26942c80234bac34b3c1352abbd9187d3e23b43dae3cf56a9f9c1ea8ee53076d' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ae12bc294a34e566579deba3e066245d09b8871dc021ef45fc715dced05297' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.21.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ab0737eebc554fb9f76042a16d68664bb2ffe6f19a92b945923200e4145848`  
		Last Modified: Thu, 23 Apr 2020 15:59:07 GMT  
		Size: 170.6 MB (170639645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:slim-stretch` - linux; 386

```console
$ docker pull rust@sha256:1fc784fe6a317670ff9d01aaf88eaac9056860360c6d71b1fb775661f22ccc77
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211381842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f048ebdaa1e7a9dab30cd4f8e55593068465f1a1851d9599477fd4039f24693a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 11:51:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.42.0
# Thu, 23 Apr 2020 11:51:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='ad1f8b5199b3b9e231472ed7aa08d2e5d1d539198a15c5b1e53c746aad81d27b' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6c6c3789dabf12171c7f500e06d21d8004b5318a5083df8b0b02c0e5ef1d017b' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='26942c80234bac34b3c1352abbd9187d3e23b43dae3cf56a9f9c1ea8ee53076d' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ae12bc294a34e566579deba3e066245d09b8871dc021ef45fc715dced05297' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.21.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c79bbb5a9f3a82c1d512e4fc9fa791c1dd911b42647180e82e2bac087c03ec`  
		Last Modified: Thu, 23 Apr 2020 11:55:22 GMT  
		Size: 188.2 MB (188240419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
