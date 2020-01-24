## `rust:alpine`

```console
$ docker pull rust@sha256:628bdacfa82a650416d90a210b8963b6d6ecf2246c8a89113b6bae97d0f48d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:a1717c7e7fe3fcc5cdf4f6fc0035d2593e43bac3257939d32ac52f65460e7247
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131087425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f143c177cbba8a4f7850059d748e5194ff8c0adb1abb57f985d8e2d34009acd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2020 05:59:59 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Fri, 24 Jan 2020 05:59:59 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.40.0
# Fri, 24 Jan 2020 06:00:13 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.20.2/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "44d689d8cf49165f059cafe10a5ce49708a26b0b0641169bc0e39ad9c54930d5 *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4894ab3ba23d1a77df9f98d547d9f3afeb033693fd523558a1e88651178b4d54`  
		Last Modified: Fri, 24 Jan 2020 06:01:10 GMT  
		Size: 34.0 MB (33983603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033dbfcf786c588de026e90e7b554f4f8c52a7cf7b94e13c79b3b187f9d9a3d`  
		Last Modified: Fri, 24 Jan 2020 06:02:39 GMT  
		Size: 94.3 MB (94316860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
