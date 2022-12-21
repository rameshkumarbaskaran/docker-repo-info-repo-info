## `erlang:25-slim`

```console
$ docker pull erlang@sha256:33aeafda0d7547358347f513b8953802203eb1de4e5711b3b14ba653933b5d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `erlang:25-slim` - linux; amd64

```console
$ docker pull erlang@sha256:1df40ceff157ac5815a18558d63d7f14f2bf1521c9bd609caf89e31b6fd4f779
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120877423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c91ef5390db1d5a90c9bf4748af9831428abce2101d78992957803f58065ba`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:21 GMT
ADD file:c13b430c8699df107ffd9ea5230b92238bc037a8e1cbbe35d6ab664941d575da in / 
# Wed, 21 Dec 2022 01:20:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:20:50 GMT
ENV OTP_VERSION=25.1.2 REBAR3_VERSION=3.19.0
# Wed, 21 Dec 2022 02:20:50 GMT
LABEL org.opencontainers.image.version=25.1.2
# Wed, 21 Dec 2022 02:25:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9ae7becd3499aeac9f94f9379e2b1b4dced4855454fe7f200a6e3e1cf4fbc53" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:25:39 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:32de3c850997ce03b6ff4ae8fb00b34b9d7d7f9a35bfcdb8538e22cc7b77c29d`  
		Last Modified: Wed, 21 Dec 2022 01:24:10 GMT  
		Size: 55.0 MB (55025166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8665328c41e6f565882aa30bdbe0b6a174aa4b4b529e74ce9aa3bc731cdc63db`  
		Last Modified: Wed, 21 Dec 2022 02:59:38 GMT  
		Size: 65.9 MB (65852257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:5399b6fac4dd51b17cda522baeb4869c37e9e3243a5bebf3a4337618aa1ffada
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109955638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf5b36391fcfdea78bf0399ffc2d514ba1a93ff3c63a8bdf8026f8c8f3f8da7`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 21 Dec 2022 01:48:53 GMT
ADD file:81ccc74e0ea343972e2f3f46d2da7e9b808d9718be44d4afa7bec6904b7ab9c6 in / 
# Wed, 21 Dec 2022 01:48:55 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:13:56 GMT
ENV OTP_VERSION=25.2 REBAR3_VERSION=3.19.0
# Wed, 21 Dec 2022 19:13:56 GMT
LABEL org.opencontainers.image.version=25.2
# Wed, 21 Dec 2022 19:18:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d33a988f39e534aff67799c5b9635612858459c9d8890772546d71ea38de897a" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:18:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:89b6e4f9f2f811282495a047e873c20d6ac2d53c72ad576a6907b1449eb3e635`  
		Last Modified: Wed, 21 Dec 2022 01:53:30 GMT  
		Size: 52.5 MB (52529974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2c7b148f3718267e86ff5f1d2a14b8929c2e6da8106cfb1f22bceff6afbdc5`  
		Last Modified: Wed, 21 Dec 2022 19:20:42 GMT  
		Size: 57.4 MB (57425664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:a2ce7e447a57c497a6c8c908730ff0867dff61526721ea3f856dd39af5cf4370
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107372950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f6861c2f4621112a91911ebce3136fd3a76d5832a0d6f4a3631d2f6393c5bb`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:09 GMT
ADD file:4b6f71680de34554595f062f9e52037b48edf19ca8f34c75877caa85c42caad3 in / 
# Wed, 21 Dec 2022 01:58:10 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 17:08:12 GMT
ENV OTP_VERSION=25.1.2 REBAR3_VERSION=3.19.0
# Wed, 21 Dec 2022 17:08:12 GMT
LABEL org.opencontainers.image.version=25.1.2
# Wed, 21 Dec 2022 17:12:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9ae7becd3499aeac9f94f9379e2b1b4dced4855454fe7f200a6e3e1cf4fbc53" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Dec 2022 17:12:16 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:706bb1d74512e1fb9ba97aa9212a32d07726fbfe77e4c7e609406d2065418f57`  
		Last Modified: Wed, 21 Dec 2022 02:04:37 GMT  
		Size: 50.2 MB (50190771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f689fc141e1112a1ae303967632cc4f42bc9cad41c2953136e8378429f7c81`  
		Last Modified: Wed, 21 Dec 2022 18:13:50 GMT  
		Size: 57.2 MB (57182179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:82f8f8803aa2676d06cb53a297ed18ab8a37c39bc67cec656a22b054c0492296
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117948777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01722cfcfe5ac4f40f957d74688399f5b932e51543007ec09dfd09e8ed7258d5`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:40 GMT
ADD file:5bbdc914ec8ed60ac85293e88ee1aafc3f0290762e320fc86dc9d79fa201834e in / 
# Wed, 21 Dec 2022 01:39:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:44:56 GMT
ENV OTP_VERSION=25.1.2 REBAR3_VERSION=3.19.0
# Wed, 21 Dec 2022 02:44:57 GMT
LABEL org.opencontainers.image.version=25.1.2
# Wed, 21 Dec 2022 02:48:03 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9ae7becd3499aeac9f94f9379e2b1b4dced4855454fe7f200a6e3e1cf4fbc53" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:48:04 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c3e6129b48b69d14c5e7a5605e2b94003fb71aac82eac46b8689f5b8007af2c5`  
		Last Modified: Wed, 21 Dec 2022 01:42:49 GMT  
		Size: 53.7 MB (53681797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b46aec3558e69548133cac22cb80cdff58a9f148c51e263b9aacfacd5cacb90`  
		Last Modified: Wed, 21 Dec 2022 03:33:21 GMT  
		Size: 64.3 MB (64266980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:dbefaf5342b968b585a684ac0c7eaeffba09a9b3624a510fb2b6fb1fb9be2554
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113634713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402db52bbae0d12e4b0bafcc06c2e352aaa72b9d606016c10bb4b929b2099854`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:08 GMT
ADD file:10d2f443f55d8ba9512899b3dff08f6e9a6c7ca096f407e3477e9798e1063785 in / 
# Wed, 21 Dec 2022 01:39:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:02:06 GMT
ENV OTP_VERSION=25.2 REBAR3_VERSION=3.19.0
# Wed, 21 Dec 2022 19:02:06 GMT
LABEL org.opencontainers.image.version=25.2
# Wed, 21 Dec 2022 19:07:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="d33a988f39e534aff67799c5b9635612858459c9d8890772546d71ea38de897a" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:07:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:bde501e1d960005aee2bdf2fc8c89b26bf694dace8740c72deda4d7705995ab7`  
		Last Modified: Wed, 21 Dec 2022 01:44:18 GMT  
		Size: 56.0 MB (56005267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b991e2d6e9ad3356456286b4c3a2c87f0a3cf05aab8076fce1d776c72cc91139`  
		Last Modified: Wed, 21 Dec 2022 19:50:56 GMT  
		Size: 57.6 MB (57629446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:b85d2b3325983d9a178cbb9ecd49305b5ee4171abcc0fed5e6707a436291304a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111449546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e04ce7b0e6dfdd0b610168c4c1b057b6d4979cd54ef6f4078fa6427d25d2be`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 21 Dec 2022 01:09:53 GMT
ADD file:972bcf9c0f583e92c03e74f66acec816703788fcc96e3a43357262f69e552ce5 in / 
# Wed, 21 Dec 2022 01:09:59 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:39:27 GMT
ENV OTP_VERSION=25.1.2 REBAR3_VERSION=3.19.0
# Wed, 21 Dec 2022 01:39:30 GMT
LABEL org.opencontainers.image.version=25.1.2
# Wed, 21 Dec 2022 02:01:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9ae7becd3499aeac9f94f9379e2b1b4dced4855454fe7f200a6e3e1cf4fbc53" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:01:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:977ef99ba351dc6668a8aa09ee6ce134ad6e6d0d9cdf1083465b1effaa1969d2`  
		Last Modified: Wed, 21 Dec 2022 01:18:00 GMT  
		Size: 53.2 MB (53245083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5247492cb9d6b3ca4fd86cd89f34ba314037d2fc39eb86dd8aa1bb3c5ced85`  
		Last Modified: Wed, 21 Dec 2022 02:24:04 GMT  
		Size: 58.2 MB (58204463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:887bbdd41da66d0b15920fe7f807482c120ec6bd0bcf4ad032736544f69aa0bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117417412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b4565fc46d2d1985a90f54421123cad1728cdbf8192c0697af213050e158d6`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:21 GMT
ADD file:c95bdb0df70fa9ce48b31a7ceb8a7be0c5b925efcf01c43595868b86994dc192 in / 
# Wed, 21 Dec 2022 01:17:25 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:31:41 GMT
ENV OTP_VERSION=25.1.2 REBAR3_VERSION=3.19.0
# Wed, 21 Dec 2022 02:31:41 GMT
LABEL org.opencontainers.image.version=25.1.2
# Wed, 21 Dec 2022 02:38:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9ae7becd3499aeac9f94f9379e2b1b4dced4855454fe7f200a6e3e1cf4fbc53" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:39:00 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:542880f4d15404af17d342ecbb76bb92724fc7cb8a91a5e18f26bd8f8811a38a`  
		Last Modified: Wed, 21 Dec 2022 01:22:46 GMT  
		Size: 58.9 MB (58897040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96ea0ce41dab3dd1c6f75ab443b96fcf549947db9a892a6732bddf0d14ada3a`  
		Last Modified: Wed, 21 Dec 2022 02:47:53 GMT  
		Size: 58.5 MB (58520372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; s390x

```console
$ docker pull erlang@sha256:10e41251f5b93de0ca00e466afbf88dbf8ca3c904fdb06de849fe2ad76da6d3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111370670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57634673b4e74ec8380ac00999ddc8b378ced180180e0fc51a1a4585f8ec3ac0`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 21 Dec 2022 01:42:51 GMT
ADD file:22c4f2d41083ce4433bec4a71e7e6ddc5bec8e44e9cf2c9f93d0874b5b4de7c3 in / 
# Wed, 21 Dec 2022 01:42:54 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:10:57 GMT
ENV OTP_VERSION=25.1.2 REBAR3_VERSION=3.19.0
# Wed, 21 Dec 2022 02:10:58 GMT
LABEL org.opencontainers.image.version=25.1.2
# Wed, 21 Dec 2022 02:20:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9ae7becd3499aeac9f94f9379e2b1b4dced4855454fe7f200a6e3e1cf4fbc53" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="ff9ef42c737480477ebdf0dd9d95ece534a14c96f05edafbf32e9af973280bc3" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:20:24 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7f45294776f4c97d23f8dbfca98d4b57701b478eedfcb154a7e7dc6d6954ba44`  
		Last Modified: Wed, 21 Dec 2022 01:48:50 GMT  
		Size: 53.3 MB (53258472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af56d10c6a72f2a3d1baace6238c5485e44819fdd9518630623e42ed6fbe42e`  
		Last Modified: Wed, 21 Dec 2022 02:31:34 GMT  
		Size: 58.1 MB (58112198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
