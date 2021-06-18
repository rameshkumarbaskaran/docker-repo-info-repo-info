## `rust:1-alpine3.12`

```console
$ docker pull rust@sha256:d0d66565e2d5d12c3eeaef8104ffc5420152e8904582cfbec33e3d1c6713e966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:1-alpine3.12` - linux; amd64

```console
$ docker pull rust@sha256:115f359134b85ce7731218cee9e308dbf228eb1e03e9ddc9b92ab7ad0157a50f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263835917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac206017e8b0d144c86f11c98c6873bbfbf895b68ce1b0b95928fdb7b9288f93`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:48:17 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 17 Jun 2021 23:24:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.53.0
# Thu, 17 Jun 2021 23:25:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331f8f29b357e0d718696e6ad746b514af26675acc6b5184af3044d23565ba11`  
		Last Modified: Thu, 15 Apr 2021 02:51:03 GMT  
		Size: 47.6 MB (47613409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93264b20f51ef92dce10bc1600cc9272030d31c50c4a52ff19c72323cf821e5d`  
		Last Modified: Thu, 17 Jun 2021 23:30:02 GMT  
		Size: 213.4 MB (213421941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be3f7285194e1ab8a9857cd2cdcae64c54baf93fbe6346109d1ead85b4fa4ce3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232666814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454bc886531968ecb2f9ebaebfeee58e30fa89679888394ba57a922a97696d86`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:09 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Tue, 15 Jun 2021 21:45:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:20:38 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Wed, 16 Jun 2021 11:20:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Wed, 16 Jun 2021 11:20:53 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='92e38262ebb9440fbdd229618eb85489d2c3d4a74c68b9ef0fdaf200e19521f8' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='4da6988d6bc80de3fa2d239f7de44152c87c257d208562ad9da17065cc08289b' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c372032f69ddd623e7e66c4200e4dc7c98f96f37cfd41b110050f7e96ead6d9`  
		Last Modified: Wed, 16 Jun 2021 11:23:05 GMT  
		Size: 38.6 MB (38561469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0a3d6748aac49e24926e295251b4281caaa879ef554d242499e6faf06b2299`  
		Last Modified: Wed, 16 Jun 2021 11:23:30 GMT  
		Size: 191.4 MB (191394651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
