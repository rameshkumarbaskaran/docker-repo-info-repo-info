## `erlang:25-slim`

```console
$ docker pull erlang@sha256:4212186bf13976380e5fb673fee7811598d995f3e337eae54eb90aa9ccf4dbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:25-slim` - linux; amd64

```console
$ docker pull erlang@sha256:71d99a96559c08932827a7816508ef025c712143f0e69ae308aafea66ef7cbdb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122416786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed7d0086d08ae56b8fd4dd9ff8fffa59e1823a26dd012152a838a240a5b2336`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 01:20:05 GMT
ADD file:68a5d7d0db592625159865110c1b7dcb15cf70ecf71b5fd541ef89584cd734ba in / 
# Wed, 11 May 2022 01:20:05 GMT
CMD ["bash"]
# Thu, 19 May 2022 21:27:34 GMT
ENV OTP_VERSION=25.0 REBAR3_VERSION=3.18.0
# Thu, 19 May 2022 21:27:34 GMT
LABEL org.opencontainers.image.version=25.0
# Thu, 19 May 2022 21:32:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5988e3bca208486494446e885ca2149fe487ee115cbc3770535fd22a795af5d2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 May 2022 21:32:07 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:67e8aa6c8bbc76b1f2bccb3864b0887671833b8667dc1f6c965fcb0eac7e6402`  
		Last Modified: Wed, 11 May 2022 01:24:45 GMT  
		Size: 54.9 MB (54945622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b6df72df64fe43482e3b3aa6eee1973ef0f0a07f2868385c195dc9ac3ac53b`  
		Last Modified: Thu, 19 May 2022 21:40:14 GMT  
		Size: 67.5 MB (67471164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:05ae646c497023609d801792e0ece1cef58c7ac6c0728bc069a4dbef3546e1f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108578429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb489f9207fd19f80add8df687bef722881a9839e15f6a784c404870c9e8f80`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 01:48:30 GMT
ADD file:d6545064ea0f75166d59e4d4a2df1e41a3477ae468e558e31f29857336978c0e in / 
# Wed, 11 May 2022 01:48:31 GMT
CMD ["bash"]
# Thu, 19 May 2022 22:11:14 GMT
ENV OTP_VERSION=25.0 REBAR3_VERSION=3.18.0
# Thu, 19 May 2022 22:11:14 GMT
LABEL org.opencontainers.image.version=25.0
# Thu, 19 May 2022 22:19:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5988e3bca208486494446e885ca2149fe487ee115cbc3770535fd22a795af5d2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 May 2022 22:19:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ba38f9a6c66968e207a7ada348a2110e3be0ff117e621d9e10ddd7c4becc0d2a`  
		Last Modified: Wed, 11 May 2022 02:03:49 GMT  
		Size: 50.1 MB (50134069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c695d6f6f6688f26d39df959fbbf964d4043a30ac6e3e505de4ed2fb3a46c4`  
		Last Modified: Thu, 19 May 2022 22:40:29 GMT  
		Size: 58.4 MB (58444360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:460eff499773498bbd8a9f896edfbcfd57ed2fb3fd30034471ac85edc2e8936e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119185153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af849be26a0d2840c1c7dc5010e07c170cb3c12b1001d39dc4580891aae282b5`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 00:46:44 GMT
ADD file:239aa42118877a929b2fbfc0d5793fee7815289280affa5286de2459385c0679 in / 
# Wed, 11 May 2022 00:46:44 GMT
CMD ["bash"]
# Thu, 19 May 2022 21:47:11 GMT
ENV OTP_VERSION=25.0 REBAR3_VERSION=3.18.0
# Thu, 19 May 2022 21:47:12 GMT
LABEL org.opencontainers.image.version=25.0
# Thu, 19 May 2022 21:51:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5988e3bca208486494446e885ca2149fe487ee115cbc3770535fd22a795af5d2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 May 2022 21:51:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3a36574378e6cece2dd3a839e1c0220eaccc4063b61d7481d1a19d3990c1f2c2`  
		Last Modified: Wed, 11 May 2022 00:53:15 GMT  
		Size: 53.6 MB (53634337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7524270f76a9e76754961ab61618ae2b0baffb532aaa32870e22df93f0c7fee`  
		Last Modified: Thu, 19 May 2022 22:01:08 GMT  
		Size: 65.6 MB (65550816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:7cb1c364be6b0c5439d9825be563722d35154eef1b5bf1d56136e1c0c2069aaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114950454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282ae0177aafcd68f7acd2d94135abdbdf9b324c46f9932d6e1c51e18fb4748f`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 01:38:57 GMT
ADD file:dae3dc662d1327f461e95b84f6f9282f3c4fb51f16ac8f20a5f141951d8436a9 in / 
# Wed, 11 May 2022 01:38:58 GMT
CMD ["bash"]
# Thu, 19 May 2022 21:46:59 GMT
ENV OTP_VERSION=25.0 REBAR3_VERSION=3.18.0
# Thu, 19 May 2022 21:47:00 GMT
LABEL org.opencontainers.image.version=25.0
# Thu, 19 May 2022 21:51:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5988e3bca208486494446e885ca2149fe487ee115cbc3770535fd22a795af5d2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 May 2022 21:51:51 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5ad4f92623738998bc77103ff64344255f842f6e5fe4a846df656351b3c4852f`  
		Last Modified: Wed, 11 May 2022 01:45:53 GMT  
		Size: 55.9 MB (55942833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061811f877a974dfb1e0585b31a0f51fed60d148fca71f133b3ac5ff7bd885a9`  
		Last Modified: Thu, 19 May 2022 22:02:40 GMT  
		Size: 59.0 MB (59007621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:b0fa1aeb6eb0859c1be30d4590356bd3be599ca5273f37c0aac8442da4c9c958
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76236df72dbe590100d647e9ca8260022aecde0598f1a88e4d773de6911edf4`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 01:31:46 GMT
ADD file:6d7393a3491f45287b6b9a4c97432db92f762fc320e7b4527fa0969250c7cda6 in / 
# Wed, 11 May 2022 01:31:53 GMT
CMD ["bash"]
# Thu, 19 May 2022 21:40:37 GMT
ENV OTP_VERSION=25.0 REBAR3_VERSION=3.18.0
# Thu, 19 May 2022 21:40:41 GMT
LABEL org.opencontainers.image.version=25.0
# Thu, 19 May 2022 21:52:03 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5988e3bca208486494446e885ca2149fe487ee115cbc3770535fd22a795af5d2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 May 2022 21:52:11 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8ad85695cd2aa86dcc7fc175edbdd1c94dbfa061000f3770d4e6f795df7d74c9`  
		Last Modified: Wed, 11 May 2022 01:42:22 GMT  
		Size: 58.8 MB (58836524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5354500e678d09938be44cbf23cf1ae49d1b48fcd6cafffc17ab76d9fb5b537b`  
		Last Modified: Thu, 19 May 2022 22:04:41 GMT  
		Size: 60.2 MB (60238521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:25-slim` - linux; s390x

```console
$ docker pull erlang@sha256:e3b0817012a276637bd4ac8f6220d29f2d3cceb5e86f7aac8d6b7b9f3d6b9d38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112629063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f4efe5d637e9c635c104c07fa9d77fed8de5f06a6c4b59e2fc693f6cc8633e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 11 May 2022 00:43:58 GMT
ADD file:8b9cfb1e16e1c11cdc1f936ccd3dfdd2104ab85b0b9078b1fe3bca89f53e0682 in / 
# Wed, 11 May 2022 00:44:00 GMT
CMD ["bash"]
# Thu, 19 May 2022 22:03:29 GMT
ENV OTP_VERSION=25.0 REBAR3_VERSION=3.18.0
# Thu, 19 May 2022 22:03:30 GMT
LABEL org.opencontainers.image.version=25.0
# Thu, 19 May 2022 22:16:42 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5988e3bca208486494446e885ca2149fe487ee115cbc3770535fd22a795af5d2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="cce1925d33240d81d0e4d2de2eef3616d4c17b0532ed004274f875e6607d25d2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 19 May 2022 22:16:50 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f8313f715dc1cdd9f8a3da73eafca06dcb30dff4c078bee35a162247cae99c4d`  
		Last Modified: Wed, 11 May 2022 00:49:41 GMT  
		Size: 53.2 MB (53208696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70931642bbd757cbb437f003185b3c611c916632667f1cc8bbf839fe854052ff`  
		Last Modified: Thu, 19 May 2022 22:34:32 GMT  
		Size: 59.4 MB (59420367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
