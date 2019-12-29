## `rust:1-slim-stretch`

```console
$ docker pull rust@sha256:5b30cf90cc7cd948207850d470e56c6bbc3014445de97716af479dd6fc69a763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-slim-stretch` - linux; amd64

```console
$ docker pull rust@sha256:72cde6bfb4d32c21d8527a00dbee9527deaf5710cb8eb3bb055602ec0590c8ae
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189328952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb2f7b2efd292320023cf695212206bc487622ec6a93f2a56d6729d4aa40c74`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sun, 29 Dec 2019 00:00:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Sun, 29 Dec 2019 00:00:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b909f2ea0d81d8429baf1f8d5ed69343707ffd3fb578737b03b8a592dbfbc7`  
		Last Modified: Sun, 29 Dec 2019 00:03:07 GMT  
		Size: 166.8 MB (166804343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-stretch` - linux; arm variant v7

```console
$ docker pull rust@sha256:96d44debbfd641d7873d11242e287bfba85fd21ae03e83c6eb2a0b27bf55d4fc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162934818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1807641c5badabb356a369f86b0ec894ccbd0932211ac957dbe7a973de4e3e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:51 GMT
ADD file:2002ba672e32ae75369830ed6a4734ce62e0118e42390b4d657f0985d6b7fd6a in / 
# Sat, 28 Dec 2019 05:03:53 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 15:23:43 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Sat, 28 Dec 2019 15:24:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:77cf262539006c8df77496f500f74a8c1edd158062440fd94d43d5b1292cefee`  
		Last Modified: Sat, 28 Dec 2019 05:11:13 GMT  
		Size: 19.3 MB (19311587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbdd2d07539c94add88be67e07030cdbd1863504d08306bd60b7f60d17d1d1d`  
		Last Modified: Sat, 28 Dec 2019 15:27:42 GMT  
		Size: 143.6 MB (143623231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-stretch` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:340eeb413211996c364496be2ce0a3b0c64c061b1386023306ae2c4e69f08788
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164548837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82943a44651d31f120b1078c54839714592f9fa8e2d30c22f56d30ab28944f62`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 23:26:29 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Sat, 28 Dec 2019 23:27:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a168c4068ed913fa866420f02fa55a2f45303ad0fdeca5ac32e5e272df4b3d`  
		Last Modified: Sat, 28 Dec 2019 23:30:03 GMT  
		Size: 144.2 MB (144163036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-stretch` - linux; 386

```console
$ docker pull rust@sha256:51de05adbfe450e2f42058374d96259cf450476b62f8fabe8fde826baaf66cb9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210290258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1e3bd06388aaad6f6f6d663b16684cd9a7aed0e8e37c6cf538bbd239d9daca`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 19:39:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Sat, 28 Dec 2019 19:40:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='e68f193542c68ce83c449809d2cad262cc2bbb99640eb47c58fc1dc58cc30add' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7c1c329a676e50c287d8183b88f30cd6afd0be140826a9fbbc0e3d717fab34d7' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='d861cc86594776414de001b96964be645c4bfa27024052704f0976dc3aed1b18' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='89f1f797dca2e5c1d75790c3c6b7be0ee473a7f4eca9663e623a41272a358da0' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.20.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67e7005a402b4f68ea5da5d5fbc8e568f31de042b0c63a48dea6f837fc2a4b4`  
		Last Modified: Sat, 28 Dec 2019 19:43:42 GMT  
		Size: 187.1 MB (187138116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
