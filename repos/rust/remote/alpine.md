## `rust:alpine`

```console
$ docker pull rust@sha256:90960c38dc98ea6c24e2944dbb5a4a8b591d99734835eed118b3a7c377e70046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:3092e38f13120eff67ea83a84512d70d0a2c26ca59b54981e60844d43c695e41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219688786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241a37466adf812b7a00b5e808fb3c270c70a3cc7609190439b8e89b4cca74ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 13:44:37 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Fri, 11 Dec 2020 13:44:37 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.48.0
# Fri, 11 Dec 2020 13:44:56 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.22.1/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "cee31c6f72b953c6293fd5d40142c7d61aa85db2a5ea81b3519fe1b492148dc9 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host x86_64-unknown-linux-musl;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f242825aded91af3766287cbfcc3751c60e0d9c663a6b461b12d853f6fba41`  
		Last Modified: Fri, 11 Dec 2020 13:46:42 GMT  
		Size: 47.6 MB (47612902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2284a12d75329adc037f32ef7479b6a5f7e2f1f813e3c18b4dc469f855aea0`  
		Last Modified: Fri, 11 Dec 2020 13:47:06 GMT  
		Size: 169.3 MB (169278939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
