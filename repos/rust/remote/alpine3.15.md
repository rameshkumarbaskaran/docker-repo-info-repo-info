## `rust:alpine3.15`

```console
$ docker pull rust@sha256:2c85f80beb26e1832bf340fdcfd773a4601d6366bf3a3a01b361a910eece266e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:alpine3.15` - linux; amd64

```console
$ docker pull rust@sha256:2734f02dd26fcd5ac6f45feb04ae06d56831d1e67d7d001e22ea12cdf46bc5cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245262938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70718bac99697002187168b5744d1c002a8f776adde70e68a423c45864df3956`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:21:45 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Wed, 10 Aug 2022 02:21:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.62.1
# Wed, 10 Aug 2022 02:22:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121c92fd9549c0b44404bcf3e79e2b5c0e83333b3e49afa29d954fbdeefc9966`  
		Last Modified: Wed, 10 Aug 2022 02:23:29 GMT  
		Size: 42.5 MB (42493423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29024032512342c75dbc9f31e48cb7c16c993936b203da312a34f3918aaabb59`  
		Last Modified: Wed, 10 Aug 2022 02:23:52 GMT  
		Size: 199.9 MB (199946003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1b02811a457c8068106feea4a2429e6d49f9fb2520a2c9866f69f71f8b4971e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243235920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400b97569fd838acdf8e4c810a862b01111b18cbb5ba7a50bf32e353bc32c253`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 06:25:06 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Wed, 10 Aug 2022 06:25:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.62.1
# Wed, 10 Aug 2022 06:25:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb5b5f8bed298d7150c992b3ba97305e95e16cbd5abeb81a5a42ce4f781623a`  
		Last Modified: Wed, 10 Aug 2022 06:27:18 GMT  
		Size: 36.1 MB (36082395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cae1b0dfa067a5cd8035a4c10cf239649a099bb320dde1518273d5c74cda040`  
		Last Modified: Wed, 10 Aug 2022 06:27:42 GMT  
		Size: 204.4 MB (204435086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
