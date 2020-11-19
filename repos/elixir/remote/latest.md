## `elixir:latest`

```console
$ docker pull elixir@sha256:9264d37d70fd9ce9c5093fa476e432fb274ec016affd70b2b58c7e84873554ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `elixir:latest` - linux; amd64

```console
$ docker pull elixir@sha256:a233428dbc7e6072f4ad9b1311ebc5acb839068cc573cb84167f961fe52ee08c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.6 MB (482577545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4457254e55e834aa15911778ce2577c27786cd0c27148c98f8d1eb89e1389a0`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Oct 2020 01:38:30 GMT
ADD file:6627ad39ea0cb9fcb212342326d14efaff51aece1fd0dc16d5bbcaa25d858622 in / 
# Tue, 13 Oct 2020 01:38:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:14:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:16:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 18:26:11 GMT
ENV OTP_VERSION=23.1.2 REBAR3_VERSION=3.14.1
# Fri, 06 Nov 2020 18:26:11 GMT
LABEL org.opencontainers.image.version=23.1.2
# Fri, 06 Nov 2020 18:39:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 06 Nov 2020 18:39:19 GMT
CMD ["erl"]
# Fri, 06 Nov 2020 18:39:19 GMT
ENV REBAR_VERSION=2.6.4
# Fri, 06 Nov 2020 18:39:25 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Fri, 06 Nov 2020 18:40:04 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="b01275b6cbdb354dcf9ed686fce2b5f9dfdd58972ded9e970e31b9215a8521f2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Fri, 06 Nov 2020 21:04:41 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Fri, 06 Nov 2020 21:06:18 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean
# Fri, 06 Nov 2020 21:06:18 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e4c3d3e4f7b024979a1c12daa4073f6353b2ba92d96418bc90451994927c9bff`  
		Last Modified: Tue, 13 Oct 2020 01:48:02 GMT  
		Size: 50.4 MB (50395978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101c41d0463bc77661fb3343235b16d536a92d2efb687046164d413e51bd4fc4`  
		Last Modified: Tue, 13 Oct 2020 02:28:35 GMT  
		Size: 7.8 MB (7811737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8275efcd805f9905d7def23603618236284b0be6b9e47455c638fbfb03fa9208`  
		Last Modified: Tue, 13 Oct 2020 02:28:35 GMT  
		Size: 10.0 MB (9996326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751620502a7a2905067c2f32d4982fb9b310b9808670ce82c0e2b40f5307a3ee`  
		Last Modified: Tue, 13 Oct 2020 02:28:53 GMT  
		Size: 51.8 MB (51829492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5e725150a20c71bdc806daa04c9c9438aed5f5a4dd376f3be66fae213b1d43`  
		Last Modified: Tue, 13 Oct 2020 02:29:32 GMT  
		Size: 192.3 MB (192263478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8985cbaa0a565d8237d9fe6be230cb01716d02cdf1d38421aaa56441e601bbf7`  
		Last Modified: Fri, 06 Nov 2020 19:10:42 GMT  
		Size: 162.2 MB (162198274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9851afe553431ce6265800267bbc74301c353cef638b31cc2364a80c13097deb`  
		Last Modified: Fri, 06 Nov 2020 19:09:49 GMT  
		Size: 196.2 KB (196228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fee4bc10f191283fb323971d41af0e148492b8d27e970a6ba54a64a6ead3455`  
		Last Modified: Fri, 06 Nov 2020 19:09:49 GMT  
		Size: 897.0 KB (897038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e38c3359c06a0dd6665e7dae65e3bf19ffa844cd8aa531300575fe2101a15c8`  
		Last Modified: Fri, 06 Nov 2020 21:11:43 GMT  
		Size: 7.0 MB (6988994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:latest` - linux; arm variant v7

```console
$ docker pull elixir@sha256:9601857774acdbf8b1d690b17f9c095a1a93c74a1e244f64a46525b763916c80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.5 MB (435549474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823749378387c93b78baf258cee41f6c59da7e0f77ca83f317378f1517d19928`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:30 GMT
ADD file:81141d8fa450e1e5af67bb3757057f3fc34d3ed35cfd0caedb0aab64c5da9aaf in / 
# Tue, 17 Nov 2020 20:20:33 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:41:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:41:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 21:42:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:45:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:44:33 GMT
ENV OTP_VERSION=23.1.2 REBAR3_VERSION=3.14.1
# Wed, 18 Nov 2020 12:44:34 GMT
LABEL org.opencontainers.image.version=23.1.2
# Wed, 18 Nov 2020 12:55:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 18 Nov 2020 12:55:52 GMT
CMD ["erl"]
# Wed, 18 Nov 2020 12:55:54 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 18 Nov 2020 12:56:08 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 18 Nov 2020 12:56:58 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="b01275b6cbdb354dcf9ed686fce2b5f9dfdd58972ded9e970e31b9215a8521f2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Thu, 19 Nov 2020 00:24:27 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Thu, 19 Nov 2020 00:26:48 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean
# Thu, 19 Nov 2020 00:26:50 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ebde10b2510128140d24e66909ceb0c80e00656af313829f82d31ae8cf08bcf8`  
		Last Modified: Tue, 17 Nov 2020 20:31:13 GMT  
		Size: 45.9 MB (45868212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05478d2a9ec4daaef33a6c87d057451c262677d02e4d9c61125bbb68bc56a601`  
		Last Modified: Tue, 17 Nov 2020 22:07:16 GMT  
		Size: 7.1 MB (7098267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c5f002cc82f5d62a78100714f451edb33a717fbf6795e309e0b1768712c093`  
		Last Modified: Tue, 17 Nov 2020 22:07:17 GMT  
		Size: 9.3 MB (9343289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d327c3810299006837433575844fea13af679784a13df32d477f1207e94ea8c`  
		Last Modified: Tue, 17 Nov 2020 22:07:42 GMT  
		Size: 47.4 MB (47356208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb9b79ac75491ca0d6be5abb23a07ad8026b4aae731e13376684bff9969e8a8`  
		Last Modified: Tue, 17 Nov 2020 22:08:38 GMT  
		Size: 168.5 MB (168486176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434666e53353cc1455adc8029b81e70f591cdf7e645bbe7360dda7d6b85bf55c`  
		Last Modified: Wed, 18 Nov 2020 14:48:16 GMT  
		Size: 149.3 MB (149315018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7756fb1176464bab2f1d643d787378216d743d3f0575a53825cc3700b7215b`  
		Last Modified: Wed, 18 Nov 2020 14:47:38 GMT  
		Size: 196.2 KB (196205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae8389d349e8b39d4502334eeb84117db2329016ac5a71af3a5ff598b370236`  
		Last Modified: Wed, 18 Nov 2020 14:47:37 GMT  
		Size: 897.0 KB (897038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4443fe34ac15f34311d0ba554356595abd9fbc1354033eb4595d46ce9ff93b`  
		Last Modified: Thu, 19 Nov 2020 00:58:44 GMT  
		Size: 7.0 MB (6989061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:latest` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:87430d7afd9cf88ea181dbbbe75f37f5772d48be5dba3aea81f615556d082fd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.7 MB (465746380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d977ed2f8a8124106c65f3193cc56e8eaa2e49b0239ed49cdaae28ec3273a6`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:04 GMT
ADD file:28343d2066831f0ffb2002914f158698f92b4af6dc16ac22e3d8e9c388c688bb in / 
# Tue, 17 Nov 2020 20:23:05 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 22:20:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:21:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 22:21:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:24:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 22:54:23 GMT
ENV OTP_VERSION=23.1.2 REBAR3_VERSION=3.14.1
# Tue, 17 Nov 2020 22:54:24 GMT
LABEL org.opencontainers.image.version=23.1.2
# Tue, 17 Nov 2020 23:04:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 17 Nov 2020 23:04:19 GMT
CMD ["erl"]
# Tue, 17 Nov 2020 23:04:20 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 17 Nov 2020 23:04:30 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Tue, 17 Nov 2020 23:05:15 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="b01275b6cbdb354dcf9ed686fce2b5f9dfdd58972ded9e970e31b9215a8521f2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Wed, 18 Nov 2020 21:43:24 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Wed, 18 Nov 2020 21:45:51 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean
# Wed, 18 Nov 2020 21:45:52 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:22518ad4a7da48a5acd01946dad2fbee99e4fca910d23b78cd7e4a16c3bd1e5b`  
		Last Modified: Tue, 17 Nov 2020 20:31:35 GMT  
		Size: 49.2 MB (49179215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ed68dbf09ea059b44b3e1013706c78f868e5f07beb5f16780ca8f52aa9594a`  
		Last Modified: Tue, 17 Nov 2020 22:36:39 GMT  
		Size: 7.7 MB (7681805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eeb09cb5ac2e2a9553920a21389f08df1b6b08c816ae4b8e60866d84119492`  
		Last Modified: Tue, 17 Nov 2020 22:36:38 GMT  
		Size: 10.0 MB (9984036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff17ea9ada38fca6de6d6808558e3c10793b90c2331b3481ad81f7c62293d8e6`  
		Last Modified: Tue, 17 Nov 2020 22:37:04 GMT  
		Size: 52.2 MB (52164616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dea92ecae615cf4291c3db4250413456b07575391a5e2b6db5ddfec7ce7a98`  
		Last Modified: Tue, 17 Nov 2020 22:37:59 GMT  
		Size: 183.8 MB (183814833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6836b83157446baf739f2d90ede7b2b6663f0d9b036b982932f74ddb64afeb29`  
		Last Modified: Wed, 18 Nov 2020 00:48:46 GMT  
		Size: 154.8 MB (154839485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4232657d74c2c74100e9e4273ac46282329f99db0590f4ed41cccd3be9f4ab87`  
		Last Modified: Wed, 18 Nov 2020 00:48:11 GMT  
		Size: 196.2 KB (196226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36a49285a3bceca423ea18fc0c77182835aa451b7bc4fdeb29aa011ecc92c87`  
		Last Modified: Wed, 18 Nov 2020 00:48:13 GMT  
		Size: 897.0 KB (897036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7d7ce8db22ba615ae71a5c388829e0950250ff11d3940e283c8f21dd40a96f`  
		Last Modified: Wed, 18 Nov 2020 22:13:43 GMT  
		Size: 7.0 MB (6989128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:latest` - linux; 386

```console
$ docker pull elixir@sha256:55da08b8cfb27667b8cd743d780fabe8db683f69acc0752425748fc30f11f2e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.0 MB (492955636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e616185e474c600af788f91c9d31e7d546a09701d5aff652e959089bfec892`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:39 GMT
ADD file:4805e11ec22df9454eb4759523111e031e84c8078bcaef178f089baca9e83cdb in / 
# Tue, 17 Nov 2020 20:19:40 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:03:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:04:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 21:04:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:06:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:41:02 GMT
ENV OTP_VERSION=23.1.2 REBAR3_VERSION=3.14.1
# Tue, 17 Nov 2020 21:41:02 GMT
LABEL org.opencontainers.image.version=23.1.2
# Tue, 17 Nov 2020 21:57:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:57:42 GMT
CMD ["erl"]
# Tue, 17 Nov 2020 21:57:42 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 17 Nov 2020 21:57:48 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Tue, 17 Nov 2020 21:58:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="b01275b6cbdb354dcf9ed686fce2b5f9dfdd58972ded9e970e31b9215a8521f2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Wed, 18 Nov 2020 16:01:51 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Wed, 18 Nov 2020 16:03:53 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean
# Wed, 18 Nov 2020 16:03:53 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:21c39c42a8e082b1b164b44e463e4752c74821dbc51451f2ac2518ae6f29dff3`  
		Last Modified: Tue, 17 Nov 2020 20:26:25 GMT  
		Size: 51.2 MB (51159492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afab7b21aa8cddd140983ed21a34965621db1efb35f635bc756479b30c3deaf3`  
		Last Modified: Tue, 17 Nov 2020 21:23:47 GMT  
		Size: 8.0 MB (7981231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a1ce1fcda982662c6c9be38bac7b53e9fd405b0b367fa902cfd957be683731`  
		Last Modified: Tue, 17 Nov 2020 21:23:46 GMT  
		Size: 10.3 MB (10338498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a190a57cc81d3d40833225fd0b5e6bf1d793a9c09ba842367e28f584fc4ab5e7`  
		Last Modified: Tue, 17 Nov 2020 21:24:09 GMT  
		Size: 53.4 MB (53433407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc286fe391b261bbe537e32cbd0af32f46ca3385b255004c032a0f243990cb02`  
		Last Modified: Tue, 17 Nov 2020 21:25:08 GMT  
		Size: 198.8 MB (198839681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6235d3d2798b12f5407d15cc13c994398323c029696d28a8bfc8baf01f1aba07`  
		Last Modified: Wed, 18 Nov 2020 01:25:43 GMT  
		Size: 163.1 MB (163121165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7543c737eef72092353aa66c549dc61a52f67ac229c750f5ca462bb933d7907d`  
		Last Modified: Wed, 18 Nov 2020 01:24:28 GMT  
		Size: 196.2 KB (196204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522445c52d269872b9344dad2aab9fbedd58e6d70a12152318988b9a42208e3`  
		Last Modified: Wed, 18 Nov 2020 01:24:29 GMT  
		Size: 897.0 KB (897040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a36c906bf6fb222c808291ce4f6dede9b8f5f069048b3630a0f3bf9451e81c`  
		Last Modified: Wed, 18 Nov 2020 16:24:17 GMT  
		Size: 7.0 MB (6988918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:latest` - linux; ppc64le

```console
$ docker pull elixir@sha256:d90219f77cdb754b273dd62f7249e07399f2db0fec75dbafeab530f5713a5c31
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.8 MB (504750822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fe93e3231c6d82a9798407bcd35960d655afa420d679f8ad63043800bd8487`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 23:22:28 GMT
ADD file:b5112ae3b22de1d8a373191ad01151a6c1cdde605887b1836672be39787e2213 in / 
# Tue, 17 Nov 2020 23:22:37 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:55:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:57:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Nov 2020 00:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 01:20:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 10:39:11 GMT
ENV OTP_VERSION=23.1.2 REBAR3_VERSION=3.14.1
# Wed, 18 Nov 2020 10:39:13 GMT
LABEL org.opencontainers.image.version=23.1.2
# Wed, 18 Nov 2020 10:54:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 18 Nov 2020 10:55:11 GMT
CMD ["erl"]
# Wed, 18 Nov 2020 10:55:15 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 18 Nov 2020 10:55:31 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 18 Nov 2020 10:56:30 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="b01275b6cbdb354dcf9ed686fce2b5f9dfdd58972ded9e970e31b9215a8521f2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Wed, 18 Nov 2020 22:21:39 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Wed, 18 Nov 2020 22:24:29 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean
# Wed, 18 Nov 2020 22:24:31 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:94e00adb98ff1f971add74025ff2a8ca87e003568d828bdb0df26ecd46c269a2`  
		Last Modified: Tue, 17 Nov 2020 23:31:43 GMT  
		Size: 54.1 MB (54143125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a46d858a6e31a5aa25fd9c527cdee95fe08fc11f45038212d1c5c7e52dc7b40`  
		Last Modified: Wed, 18 Nov 2020 01:53:05 GMT  
		Size: 8.3 MB (8255326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfab907b4d9fde9fb35f17a366b653e709c31cbce8602a2ae23c23d39524820`  
		Last Modified: Wed, 18 Nov 2020 01:53:06 GMT  
		Size: 10.7 MB (10727375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157cce210a3874859c02d469911ddfc967ed435c3c04ebf12cdad81fe199cef0`  
		Last Modified: Wed, 18 Nov 2020 01:54:24 GMT  
		Size: 57.5 MB (57455140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c205957dfc9cb35b737f51ec6985e8bbfa793cabfde43085a053e7f5cf44ac`  
		Last Modified: Wed, 18 Nov 2020 01:57:37 GMT  
		Size: 203.1 MB (203086260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d406115b682a8086ce1457daef27aeca67abb7c8df41201781a3b2d868a2f79`  
		Last Modified: Wed, 18 Nov 2020 11:41:16 GMT  
		Size: 163.0 MB (163001227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a745f6bf8fe2db04c1fbf668caff75992e0d9a23f9e9ea1a1f82512a075cd72`  
		Last Modified: Wed, 18 Nov 2020 11:40:04 GMT  
		Size: 196.2 KB (196188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557285aec647c0e29967961112f02059848fc8f708f9dcd60eeb6728a324d774`  
		Last Modified: Wed, 18 Nov 2020 11:40:05 GMT  
		Size: 897.0 KB (897040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338b9b1056eeea607e5894201d1a2ae3dfaf86459d71de507a054f782e92dd4`  
		Last Modified: Wed, 18 Nov 2020 22:42:27 GMT  
		Size: 7.0 MB (6989141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:latest` - linux; s390x

```console
$ docker pull elixir@sha256:dc456c042faaffb8cc6f9559814e735976a555e703b286d65cff47494e498fad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.6 MB (458588477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d74340e30750ea330dc02f251cd88cd04babc670fd6b58956a0200275dac49`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 17 Nov 2020 20:17:56 GMT
ADD file:dfb1d2f775a9c4493397d0ca05aa6486393c6dad4f0fb5f48ffd209397301bdb in / 
# Tue, 17 Nov 2020 20:18:05 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 21:32:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:32:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Nov 2020 21:32:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 21:35:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:33:45 GMT
ENV OTP_VERSION=23.1.2 REBAR3_VERSION=3.14.1
# Wed, 18 Nov 2020 00:33:45 GMT
LABEL org.opencontainers.image.version=23.1.2
# Wed, 18 Nov 2020 00:51:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="afff83ab51830cb7d9ed995d0c98a3947896471cde9af000befd78b390f109be" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:51:49 GMT
CMD ["erl"]
# Wed, 18 Nov 2020 00:51:49 GMT
ENV REBAR_VERSION=2.6.4
# Wed, 18 Nov 2020 00:52:00 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Wed, 18 Nov 2020 00:52:56 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="b01275b6cbdb354dcf9ed686fce2b5f9dfdd58972ded9e970e31b9215a8521f2" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
# Wed, 18 Nov 2020 21:06:48 GMT
ENV ELIXIR_VERSION=v1.11.2 LANG=C.UTF-8
# Wed, 18 Nov 2020 21:09:27 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="318f0a6cb372186b0cf45d2e9c9889b4c9e941643fd67ca0ab1ec32710ab6bf5" 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean
# Wed, 18 Nov 2020 21:09:29 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6e95a7d20e6bbf957d2bb5912f19784daba6953d8afac5562453108dd45940e1`  
		Last Modified: Tue, 17 Nov 2020 20:23:18 GMT  
		Size: 49.0 MB (48968246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab56d289be912cd903623a00b35bdc52f4f1b54a6778c1ba4c076e5cfe339aa5`  
		Last Modified: Tue, 17 Nov 2020 21:48:36 GMT  
		Size: 7.4 MB (7385996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29ee109f7efbe0700da6e225717912b22d8e015d8d9a9968e564419b1ba97a3`  
		Last Modified: Tue, 17 Nov 2020 21:48:36 GMT  
		Size: 9.9 MB (9882242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e45adeb409573e310b14d50aaf13f2a71a45e62f9f872239e36eb86f927b54`  
		Last Modified: Tue, 17 Nov 2020 21:50:38 GMT  
		Size: 51.4 MB (51380183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29eec538f7c27dd46ca5cff5bd6e29299adea0933747804e60e0dc381865c13d`  
		Last Modified: Tue, 17 Nov 2020 21:53:15 GMT  
		Size: 176.8 MB (176833166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2dcff426a5c5beaa9da1e6c66132bc60f7208b5cd672f129490ccf6241b12e`  
		Last Modified: Wed, 18 Nov 2020 01:29:36 GMT  
		Size: 156.1 MB (156056358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c9c6a52fee8567d3e27ec613af6ef4b77bbb792b303f3a5ee7d43b694a05b8`  
		Last Modified: Wed, 18 Nov 2020 01:29:13 GMT  
		Size: 196.2 KB (196186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b84d06df900c1a087e7b8edef8917acf2022b21351f09569d79f73de9d67508`  
		Last Modified: Wed, 18 Nov 2020 01:29:12 GMT  
		Size: 897.0 KB (897039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa900ee0a6bb6104cabf003e526681a93102962fd23df06f3d9c7fcd702c6796`  
		Last Modified: Wed, 18 Nov 2020 21:23:56 GMT  
		Size: 7.0 MB (6989061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
