## `erlang:24-slim`

```console
$ docker pull erlang@sha256:f4dd9fb3b0bc7da418d75f01a79a6920ca07987f826cdf0bf7dc89ce9c234e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:24-slim` - linux; amd64

```console
$ docker pull erlang@sha256:51240353b592af61fd8c5438d9a4312405efb492e6a26f5dd4912188add88421
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118597914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d212721139f0a31bb1ab0ed69414f214b43a44463475cb09e74a3a1c8ef0e0`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:51 GMT
ADD file:cb5ed7070880d4c0177fbe6dd278adb7926e38cd73e6abd582fd8d67e4bbf06c in / 
# Wed, 17 Nov 2021 02:20:51 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 00:31:44 GMT
ENV OTP_VERSION=24.1.7 REBAR3_VERSION=3.17.0
# Tue, 23 Nov 2021 00:31:44 GMT
LABEL org.opencontainers.image.version=24.1.7
# Tue, 23 Nov 2021 00:39:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1dd1a238f1f3e79784b902f3cd00e06f35a630191eaf73324a07a26a2c93af3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 23 Nov 2021 00:39:21 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1230f17f526cb07307d41462355b10488b994e8bdafe0d8f275a405fa3b33831`  
		Last Modified: Wed, 17 Nov 2021 02:26:06 GMT  
		Size: 50.4 MB (50437098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db13ede85378c23119d6723de12be67cae58b8396decf7fc2e9813908c0f575`  
		Last Modified: Tue, 23 Nov 2021 00:58:11 GMT  
		Size: 68.2 MB (68160816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:24-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:1baf371e84a8b95b26d84c263ad0d7462ea49f98b1128fb9875931bed759dcc9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104940864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a150079473f59f0b3a124984308ce3e35c48ccf971bf261e8871a1913953da9f`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Fri, 19 Nov 2021 18:09:55 GMT
ENV OTP_VERSION=24.1.6 REBAR3_VERSION=3.17.0
# Fri, 19 Nov 2021 18:09:55 GMT
LABEL org.opencontainers.image.version=24.1.6
# Fri, 19 Nov 2021 18:17:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1b0db74f01f0072299347b794b51d170bf1b71a8f9b6c0aac404ed2c440611ad" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 19 Nov 2021 18:17:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea6cd88b58ec95bcce208eee410fae2319089b37e841baf22bbc4e1af642ebd`  
		Last Modified: Fri, 19 Nov 2021 18:37:06 GMT  
		Size: 59.0 MB (59022765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:24-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:597f8ca4be7b506f2007ae3ac2ef3ec001832f464c20146e80877a67e51fe23f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109265531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac05a334312559ea5ef1344ca913d2084a268ab4a7c12e4cfdc2b7ce86ff103`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 00:45:38 GMT
ENV OTP_VERSION=24.1.7 REBAR3_VERSION=3.17.0
# Tue, 23 Nov 2021 00:45:39 GMT
LABEL org.opencontainers.image.version=24.1.7
# Tue, 23 Nov 2021 00:49:37 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1dd1a238f1f3e79784b902f3cd00e06f35a630191eaf73324a07a26a2c93af3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 23 Nov 2021 00:49:38 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7694fa302da2e4d11917cb9941a5e4378b8f06ffcecc387a297032caa65784`  
		Last Modified: Tue, 23 Nov 2021 00:58:42 GMT  
		Size: 60.0 MB (60042541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:24-slim` - linux; 386

```console
$ docker pull erlang@sha256:7d859e2db29f9a636a227287e9e3eaa5233f555a7b5c8222e4c5b6f3c37abc37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111160804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaa8ef93a133a2975c4ceef3b08aa2f44e0245c5c41d047ee397cfc5ceab093`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:06 GMT
ADD file:87367b4870b0dc997a37b7648ff6efa8e42bed68b0573be2ade992c206fbdd2e in / 
# Wed, 17 Nov 2021 02:40:07 GMT
CMD ["bash"]
# Fri, 19 Nov 2021 19:00:11 GMT
ENV OTP_VERSION=24.1.6 REBAR3_VERSION=3.17.0
# Fri, 19 Nov 2021 19:00:11 GMT
LABEL org.opencontainers.image.version=24.1.6
# Fri, 19 Nov 2021 19:07:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1b0db74f01f0072299347b794b51d170bf1b71a8f9b6c0aac404ed2c440611ad" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 19 Nov 2021 19:07:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1f740e90292e8fcb22dbbbdbe335252fd87d406cd6e139738853fc65c8bb54f4`  
		Last Modified: Wed, 17 Nov 2021 02:48:17 GMT  
		Size: 51.2 MB (51207728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e028042a289e9d2459dfcfcd103879bd0f283acc39c8a6113b95173e5feecb`  
		Last Modified: Fri, 19 Nov 2021 19:21:29 GMT  
		Size: 60.0 MB (59953076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:24-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:31ea3f315e0e2c0624553266d1b375d0c133f89570b70e85f13f64f5f56bcb2f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115080863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890eeb0b437f2d395052f0fc486d900db0474cb81b7c0827a367f5d7ae3be177`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Nov 2021 03:29:10 GMT
ADD file:fc0d43ba74311deef20b2131cca3a8e86b083624d63560251191adca21417f2f in / 
# Wed, 17 Nov 2021 03:29:20 GMT
CMD ["bash"]
# Fri, 19 Nov 2021 18:32:31 GMT
ENV OTP_VERSION=24.1.6 REBAR3_VERSION=3.17.0
# Fri, 19 Nov 2021 18:32:33 GMT
LABEL org.opencontainers.image.version=24.1.6
# Fri, 19 Nov 2021 18:44:04 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1b0db74f01f0072299347b794b51d170bf1b71a8f9b6c0aac404ed2c440611ad" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 19 Nov 2021 18:44:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:aad6e1fe6f7c56b0e1b5850f40e4fec91ffaed4b6235e730f5c7ff43db397d3d`  
		Last Modified: Wed, 17 Nov 2021 03:56:39 GMT  
		Size: 54.2 MB (54183702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca600b341feaa5758a93c78c628ce20b9c169b778e8074927400def8f18a081`  
		Last Modified: Fri, 19 Nov 2021 18:55:16 GMT  
		Size: 60.9 MB (60897161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:24-slim` - linux; s390x

```console
$ docker pull erlang@sha256:5efc5e511fa209337fc9f37689fc13a4023b84288aa6f382b3610bc18d9caf09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109097923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f83a895ee874a408fa98af40f405635afbc0ed1e09be9ebecaa8b6d5c6c522c`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:40 GMT
ADD file:dc4ee96f81059accdc88a686f80f1714bc9d2f383af71c0d130c08560cea115e in / 
# Wed, 17 Nov 2021 02:42:42 GMT
CMD ["bash"]
# Tue, 23 Nov 2021 00:47:42 GMT
ENV OTP_VERSION=24.1.7 REBAR3_VERSION=3.17.0
# Tue, 23 Nov 2021 00:47:42 GMT
LABEL org.opencontainers.image.version=24.1.7
# Tue, 23 Nov 2021 00:51:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1dd1a238f1f3e79784b902f3cd00e06f35a630191eaf73324a07a26a2c93af3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 23 Nov 2021 00:51:35 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c12eae84d2674466d924a139a276e361afa9f63de21cf77eae19bd94eaac2629`  
		Last Modified: Wed, 17 Nov 2021 02:48:42 GMT  
		Size: 49.0 MB (49005439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041c46d4509c0bfc56f231361f8793ae59c96eb3230ce147feecbd5f0c3d1b10`  
		Last Modified: Tue, 23 Nov 2021 00:58:29 GMT  
		Size: 60.1 MB (60092484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
