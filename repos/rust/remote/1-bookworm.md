## `rust:1-bookworm`

```console
$ docker pull rust@sha256:ba4ebbf3660f268f6e97352e4ddc7f031d7afa93e5264131f0b13ebfbabbe677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:1d6a596d5d707b58feed1bbf0270529098c91f94b32752f00d2098926ae12a1e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.0 MB (520007696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee767ffc6db2bdf8b88073ac561056a4293a92ab12e71be9e7080d970034b567`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:19:36 GMT
ADD file:99a61197d7273704581c44eae01f3342e9f3562e84fe66cc2d56ce563e58450a in / 
# Thu, 09 Feb 2023 03:19:37 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:08:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 09:09:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:10:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Feb 2023 19:14:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.67.1
# Fri, 10 Feb 2023 19:14:36 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:45c04dd46fbf614b423b54561d34c6339a0376d1717729ef6dcf101dbfd20f8c`  
		Last Modified: Thu, 09 Feb 2023 03:24:14 GMT  
		Size: 49.1 MB (49054961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666db2f0c3920c26fca8be06c139f8e93863caba116d9677e3ca33d4f46a074f`  
		Last Modified: Thu, 09 Feb 2023 09:16:52 GMT  
		Size: 9.0 MB (9033134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887d37599cf7cd74d72dc9d56f19300520564439f19992bb2e8de2ce584df713`  
		Last Modified: Thu, 09 Feb 2023 09:16:52 GMT  
		Size: 11.4 MB (11354763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9f5103cc59ff9f92590beaed1d1a0320afb6a600adac22bfb4497e37e008a7`  
		Last Modified: Thu, 09 Feb 2023 09:17:10 GMT  
		Size: 64.4 MB (64416604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d2abc48fa610a6001247fdf6c328c8999aa6f06f48d92d788a037fff8b302e`  
		Last Modified: Thu, 09 Feb 2023 09:17:46 GMT  
		Size: 210.7 MB (210719933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff9b6dc3d6c6a3b9e8cdde1d499453da0cb84182eadb871ae7bc8d17a858e5c`  
		Last Modified: Fri, 10 Feb 2023 19:20:29 GMT  
		Size: 175.4 MB (175428301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:a6063faa473718896948cb8aeca213a927c949649a1e1e3deba2e2bf89dc0505
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.0 MB (507952656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ed5e38ff77a32b6e9e1396f8ed8cc9afdd0c54e53d5336bd1652230274763c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 06:11:15 GMT
ADD file:00a7b86df7c1e3b1064f9848e66b835d60203374321048b004728889f9033be6 in / 
# Thu, 09 Feb 2023 06:11:17 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 17:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 17:35:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 17:35:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 17:36:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Feb 2023 05:38:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.67.1
# Fri, 10 Feb 2023 05:39:01 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:cc1adfc8958bbc0fb16a7e0a1534193e67c7436227ac284a68c36601ef15914c`  
		Last Modified: Thu, 09 Feb 2023 06:18:07 GMT  
		Size: 45.8 MB (45795912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7377a44228d605548594ad5afaed8f41257a1d7a090828d18171500dabe541`  
		Last Modified: Thu, 09 Feb 2023 17:45:53 GMT  
		Size: 8.1 MB (8124839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c807de20421b260151ee3eb132429b34a5c6336f5e0d0b16dcab34dbc01809c`  
		Last Modified: Thu, 09 Feb 2023 17:45:53 GMT  
		Size: 10.6 MB (10635770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403dac43fbe1292186670418f1f2d9137b55d87c6d38dbe1761e8b31b11995aa`  
		Last Modified: Thu, 09 Feb 2023 17:46:15 GMT  
		Size: 59.6 MB (59595816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929d9e0459daced8ab6f2821d09b170f926dbb9590357db57c48a7deae39bc99`  
		Last Modified: Thu, 09 Feb 2023 17:46:53 GMT  
		Size: 174.8 MB (174781630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322127e822104392b368993593445333c66ba8576c3759cf2a0b817dc56bc1d3`  
		Last Modified: Fri, 10 Feb 2023 05:46:10 GMT  
		Size: 209.0 MB (209018689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d7d1d2453362327a95e3c90d44a23153f8543678210dc7c72c13913434efdf0b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.1 MB (577076171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a02412b1aa7f2fe0d9510f26bc954c989e1614f337af3e8bc230b669356def`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:10 GMT
ADD file:bb3880a9ad854cde236b0e81a38e30cc0a4164d2d9ef140f29c28314ad31223d in / 
# Thu, 09 Feb 2023 03:58:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:06:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 09:06:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:07:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 21:33:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.67.1
# Thu, 09 Feb 2023 21:34:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:65cbd465e3f6368144b4429f3d79a2ef3faba24e97c701076009f84c0ed82a6a`  
		Last Modified: Thu, 09 Feb 2023 04:01:39 GMT  
		Size: 49.1 MB (49105777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95aa4eba0cc6b3f79d40a859b9545ba8a7d82ca90ca963ffb0d8b8aceeb9794`  
		Last Modified: Thu, 09 Feb 2023 09:13:24 GMT  
		Size: 8.9 MB (8865552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4af4383486dc9f58a0ce41730a60fc0d02f4751b99f733f5a6892ab841ea456`  
		Last Modified: Thu, 09 Feb 2023 09:13:25 GMT  
		Size: 11.3 MB (11319820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e4f09b81041b1ebe6ac8c4c6598c178218f530c037c945ff427b3ae385d4fc`  
		Last Modified: Thu, 09 Feb 2023 09:13:41 GMT  
		Size: 64.3 MB (64312153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6cf3d4e8a9eef9cb35c04005462a9c014a85fe85997a832a716fc1c3af19da`  
		Last Modified: Thu, 09 Feb 2023 09:14:11 GMT  
		Size: 202.1 MB (202138539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702e23f8a057deb920b652160bb0a68ccb133a456b568dbd558303ae2b126ff2`  
		Last Modified: Thu, 09 Feb 2023 21:40:33 GMT  
		Size: 241.3 MB (241334330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:62c74bcc51e27515d43d07b3fe94cbf3933b2c5936729669d42906ca5f11c480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.1 MB (537133419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede7bbe78a956166c535e8489255c520ec71e3329626c34d7127dbe7c5503222`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 05:12:11 GMT
ADD file:37cc85485a8f79a4bd5557a42685805da0b367ff061d53fdf29d5f242593ea1d in / 
# Thu, 09 Feb 2023 05:12:12 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:15:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 12:16:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:17:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Feb 2023 00:09:07 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.67.1
# Fri, 10 Feb 2023 00:09:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:0153a17486e7cd96c30b54f1d68ab1cffaca99de43335324f16477807b1ddb1c`  
		Last Modified: Thu, 09 Feb 2023 05:17:35 GMT  
		Size: 50.1 MB (50089500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed8e4b1c1724684d6e2a33bc3846f758a9ab930a989ca696a47b758ccc1d3c9`  
		Last Modified: Thu, 09 Feb 2023 12:24:13 GMT  
		Size: 9.2 MB (9211678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191a31a7f1a5ee7a1fb212c4b04edd4ca2f9180c9ea83ed8a801bb4717394a6c`  
		Last Modified: Thu, 09 Feb 2023 12:24:13 GMT  
		Size: 11.6 MB (11557538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa4d52e1ad267c20b5cc8237e96edf4b2761f942a471ff6c8fccb7f813b5b4f`  
		Last Modified: Thu, 09 Feb 2023 12:24:33 GMT  
		Size: 66.3 MB (66298863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1328233c31db750411ab179cbf816f658ac4e695cf83e1b81d64de5c5a655b68`  
		Last Modified: Thu, 09 Feb 2023 12:25:08 GMT  
		Size: 209.6 MB (209638394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683de355dea795ac8885d3248e6c13f948a2252a1033395d6de9c673ecdcda3e`  
		Last Modified: Fri, 10 Feb 2023 00:15:09 GMT  
		Size: 190.3 MB (190337446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
