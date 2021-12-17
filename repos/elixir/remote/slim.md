## `elixir:slim`

```console
$ docker pull elixir@sha256:52daf4b1cb70a9e91758baadf100bcf6e7a6b568e34eaa85c2bba25d4ded3672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `elixir:slim` - linux; amd64

```console
$ docker pull elixir@sha256:7815e1be6db6b86459515b3acdfba34fc48b0868be8e7e1a24ddea2068dbfdc3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125655567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f549f378e254330d5db550d1147d2cd79cb17185dbf2273d3117700a688afb`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Fri, 17 Dec 2021 18:31:34 GMT
ENV OTP_VERSION=24.2 REBAR3_VERSION=3.17.0
# Fri, 17 Dec 2021 18:31:34 GMT
LABEL org.opencontainers.image.version=24.2
# Fri, 17 Dec 2021 18:39:00 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0b9c9ba7d8b40f6c77d529e07561b10f0914d2bfe9023294d7eda85b62936792" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 17 Dec 2021 18:39:01 GMT
CMD ["erl"]
# Fri, 17 Dec 2021 19:50:50 GMT
ENV ELIXIR_VERSION=v1.13.1 LANG=C.UTF-8
# Fri, 17 Dec 2021 19:51:48 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="deaba8156b11777adfa28e54e76ddf49ab1a0132cca54c41d9d7648e800edcc8" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 Dec 2021 19:51:48 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad8182aadf6644e0911debaba4d47cb67e3d621ed8e008cc6115e19b4f0b158`  
		Last Modified: Fri, 17 Dec 2021 18:57:47 GMT  
		Size: 64.3 MB (64292046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fba84f7f600160e9dab8e349eaebfb18b92baf21ba93906b9c9f6570a567621`  
		Last Modified: Fri, 17 Dec 2021 19:59:08 GMT  
		Size: 6.4 MB (6430643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:382403a4f099520268822f1b6a27f7395de36fff1fb99317a43a5c1bdd3aa5f1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113459121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed0da1bbdfae5a3b28dc82b85db2fc6e7e0a42ae45f2635c03b4b12888e56e3`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 02 Dec 2021 09:04:39 GMT
ADD file:f0d0256a657fcc82cba38ec9fe377ae4d30125de11e0003de81177370592b440 in / 
# Thu, 02 Dec 2021 09:04:40 GMT
CMD ["bash"]
# Fri, 17 Dec 2021 18:10:21 GMT
ENV OTP_VERSION=24.2 REBAR3_VERSION=3.17.0
# Fri, 17 Dec 2021 18:10:21 GMT
LABEL org.opencontainers.image.version=24.2
# Fri, 17 Dec 2021 18:18:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0b9c9ba7d8b40f6c77d529e07561b10f0914d2bfe9023294d7eda85b62936792" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 17 Dec 2021 18:18:39 GMT
CMD ["erl"]
# Fri, 17 Dec 2021 18:59:15 GMT
ENV ELIXIR_VERSION=v1.13.1 LANG=C.UTF-8
# Fri, 17 Dec 2021 19:01:45 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="deaba8156b11777adfa28e54e76ddf49ab1a0132cca54c41d9d7648e800edcc8" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 Dec 2021 19:01:45 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e704987a22630df63d8518dd22b13ec2a4f460fd492ab42b97cdc6f971e7be31`  
		Last Modified: Thu, 02 Dec 2021 09:20:17 GMT  
		Size: 50.1 MB (50134315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffd573447ac103444d589c09ec49697f36a7f9e2f75569733250ed9eb554a7a`  
		Last Modified: Fri, 17 Dec 2021 18:37:43 GMT  
		Size: 56.9 MB (56894548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622a0769e0abd5f6d455ed6db4765b7339afed9db6b7eb7fc792b1154db30d73`  
		Last Modified: Fri, 17 Dec 2021 19:22:18 GMT  
		Size: 6.4 MB (6430258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:143014e4b6b396883049ef1cce6109219d0144349383b02bf4444cde3b623bef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117751645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed0917c827b08747f1b363b5fa5cf88b77c84e456085327245ee27ef63b8658`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Fri, 17 Dec 2021 18:46:10 GMT
ENV OTP_VERSION=24.2 REBAR3_VERSION=3.17.0
# Fri, 17 Dec 2021 18:46:11 GMT
LABEL org.opencontainers.image.version=24.2
# Fri, 17 Dec 2021 18:50:12 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0b9c9ba7d8b40f6c77d529e07561b10f0914d2bfe9023294d7eda85b62936792" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 17 Dec 2021 18:50:13 GMT
CMD ["erl"]
# Fri, 17 Dec 2021 19:25:12 GMT
ENV ELIXIR_VERSION=v1.13.1 LANG=C.UTF-8
# Fri, 17 Dec 2021 19:26:11 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="deaba8156b11777adfa28e54e76ddf49ab1a0132cca54c41d9d7648e800edcc8" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 Dec 2021 19:26:11 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b2ec9ce37b82f3bdd6b8064a78431e1ea22df4d59b183157c76f6c5c469b76`  
		Last Modified: Fri, 17 Dec 2021 18:59:09 GMT  
		Size: 57.7 MB (57702450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32784107dd0631b90585be9769838c1268817610edab8ea31ee4dda662cf117a`  
		Last Modified: Fri, 17 Dec 2021 19:35:16 GMT  
		Size: 6.4 MB (6430168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:30244a8bce780d3eeecba1d68f5748e4ad53d414027ddfd5e0ebbf9af1cbbecd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119733328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31e162e82197e84879c4537f05a5d5a529b2a624b29148a701d6ae1873ff8fe`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:37 GMT
ADD file:0fd00a1dc1745744d1e95964f1f6fc73e016055aeec062f1946440b6ba68411d in / 
# Thu, 02 Dec 2021 02:39:37 GMT
CMD ["bash"]
# Fri, 17 Dec 2021 18:58:35 GMT
ENV OTP_VERSION=24.2 REBAR3_VERSION=3.17.0
# Fri, 17 Dec 2021 18:58:35 GMT
LABEL org.opencontainers.image.version=24.2
# Fri, 17 Dec 2021 19:06:38 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0b9c9ba7d8b40f6c77d529e07561b10f0914d2bfe9023294d7eda85b62936792" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 17 Dec 2021 19:06:38 GMT
CMD ["erl"]
# Fri, 17 Dec 2021 19:39:25 GMT
ENV ELIXIR_VERSION=v1.13.1 LANG=C.UTF-8
# Fri, 17 Dec 2021 19:40:50 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="deaba8156b11777adfa28e54e76ddf49ab1a0132cca54c41d9d7648e800edcc8" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 Dec 2021 19:40:51 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3dfa4acb9eec45f56cd836373cf9bf145fb45d1ae4cbc3181c21d4d01d14037d`  
		Last Modified: Thu, 02 Dec 2021 02:47:22 GMT  
		Size: 55.9 MB (55937571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf392b1a29b006bc7fcd3ec4f8d25cc7c411857555dd56cb3a08432d3fc63b24`  
		Last Modified: Fri, 17 Dec 2021 19:20:33 GMT  
		Size: 57.4 MB (57365435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef0490dc1fe793349b2116fddf61c17c9d82a298d045f735060efdde9495d4f`  
		Last Modified: Fri, 17 Dec 2021 19:51:31 GMT  
		Size: 6.4 MB (6430322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:2fdc026b66936bec644819fa9c3fa52e5b9fbbcb09600ff251c741d133a58dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123552343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c64b3f598ae8efd0adb3164b7ce4d00a5e9e76a8a09785f295e2fd4774abb24`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 02 Dec 2021 07:20:49 GMT
ADD file:781003f73ff5fb7313d2bd58dc99ae83adc49c419929d32a63c29a9d45b5a554 in / 
# Thu, 02 Dec 2021 07:20:54 GMT
CMD ["bash"]
# Fri, 17 Dec 2021 18:30:17 GMT
ENV OTP_VERSION=24.2 REBAR3_VERSION=3.17.0
# Fri, 17 Dec 2021 18:30:18 GMT
LABEL org.opencontainers.image.version=24.2
# Fri, 17 Dec 2021 18:39:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0b9c9ba7d8b40f6c77d529e07561b10f0914d2bfe9023294d7eda85b62936792" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 17 Dec 2021 18:39:36 GMT
CMD ["erl"]
# Fri, 17 Dec 2021 19:09:12 GMT
ENV ELIXIR_VERSION=v1.13.1 LANG=C.UTF-8
# Fri, 17 Dec 2021 19:11:43 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="deaba8156b11777adfa28e54e76ddf49ab1a0132cca54c41d9d7648e800edcc8" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 Dec 2021 19:11:44 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6ae53eb717439cac2dd934aaff8829ad7eadd86024d1ea6efc5bcd9ad4291200`  
		Last Modified: Thu, 02 Dec 2021 07:31:08 GMT  
		Size: 58.8 MB (58819590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c69906c924dfcde0895c260d607334efb046511f626396fe3674e16ecefe68`  
		Last Modified: Fri, 17 Dec 2021 18:50:08 GMT  
		Size: 58.3 MB (58301520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead9e3378877ab748c16d10d74773e19f117848376ae4c566c7c70a0aa6136a1`  
		Last Modified: Fri, 17 Dec 2021 19:25:10 GMT  
		Size: 6.4 MB (6431233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:f91ef5fde77c9e53ebfbb556473b0df64907585d515b508b6e61c221ce7667ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117457297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4603d3dfc8adb4d332c0574cefc4ea1da74884adec3618d4f5e00aafeb7d240f`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 02 Dec 2021 07:18:46 GMT
ADD file:56acf855563ce8cc885f3c7619508d25f809dd0547557b5e6ed0aa9fd55266f2 in / 
# Thu, 02 Dec 2021 07:18:50 GMT
CMD ["bash"]
# Fri, 17 Dec 2021 18:47:55 GMT
ENV OTP_VERSION=24.2 REBAR3_VERSION=3.17.0
# Fri, 17 Dec 2021 18:47:55 GMT
LABEL org.opencontainers.image.version=24.2
# Fri, 17 Dec 2021 18:52:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0b9c9ba7d8b40f6c77d529e07561b10f0914d2bfe9023294d7eda85b62936792" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 17 Dec 2021 18:52:04 GMT
CMD ["erl"]
# Fri, 17 Dec 2021 19:16:29 GMT
ENV ELIXIR_VERSION=v1.13.1 LANG=C.UTF-8
# Fri, 17 Dec 2021 19:17:18 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="deaba8156b11777adfa28e54e76ddf49ab1a0132cca54c41d9d7648e800edcc8" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 Dec 2021 19:17:19 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:f0bfe5b50d4f7032d3e697cb821ab18746c1148d2bf1076e29427de01f0f0d31`  
		Last Modified: Thu, 02 Dec 2021 07:24:51 GMT  
		Size: 53.2 MB (53207427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a0c88b066e85eb792655f86759afa522bd0b13c5f4f3d303b9409d50b7d489`  
		Last Modified: Fri, 17 Dec 2021 18:59:10 GMT  
		Size: 57.8 MB (57819621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a19c84c8b4b083e97db9a020e65d727da5f118fb04b9121c8071fa95663f99`  
		Last Modified: Fri, 17 Dec 2021 19:24:26 GMT  
		Size: 6.4 MB (6430249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
