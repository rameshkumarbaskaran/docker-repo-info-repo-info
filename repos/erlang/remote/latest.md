## `erlang:latest`

```console
$ docker pull erlang@sha256:cb02f53fc3d9567188b5610518cdcf21821bbd7f258d1dfcbf93b490614a91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:latest` - linux; amd64

```console
$ docker pull erlang@sha256:23d09c3777d4bb0fefe0d7ef05b1b81ead864119384aa3a4148d9fae09400688
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.1 MB (486080407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4136cb3c8cc9cd2957848f0d49caaf3d4af601fab084a00e3cf229ee7c299a`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:41:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:42:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:43:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 04:05:44 GMT
ENV OTP_VERSION=24.1.7 REBAR3_VERSION=3.17.0
# Thu, 02 Dec 2021 04:05:44 GMT
LABEL org.opencontainers.image.version=24.1.7
# Thu, 02 Dec 2021 04:25:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1dd1a238f1f3e79784b902f3cd00e06f35a630191eaf73324a07a26a2c93af3" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 02 Dec 2021 04:25:30 GMT
CMD ["erl"]
# Thu, 02 Dec 2021 04:25:30 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 02 Dec 2021 04:25:35 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 02 Dec 2021 04:26:16 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c54d048f1f1a1f28079caa54bf5d99803f937ffe5c1dc6e207698f70b4e74`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 7.8 MB (7833819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368544993b2deeeffdd19463cdf92ec4e39f83073de5de316f9f5c725ab403f`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 10.0 MB (9997240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9d1af719764344a5a57ac06d5f23a36bdca0aeec69294d60ab5c898ca87b38`  
		Last Modified: Thu, 02 Dec 2021 03:51:05 GMT  
		Size: 51.8 MB (51841246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8ae1e274f45ffac8ea08442a90df704a97507417982171a6c7c5c7798a04e5`  
		Last Modified: Thu, 02 Dec 2021 03:51:43 GMT  
		Size: 192.4 MB (192425108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8566e595e9369fbdc3134fb0445597d2d2d2f5c3ecf49ad0750e54e6c20d8ddb`  
		Last Modified: Thu, 02 Dec 2021 09:16:06 GMT  
		Size: 172.4 MB (172390786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc71194f5092e2f24a8033280b50c7ab792f95175422d9a15335461d64719e9`  
		Last Modified: Thu, 02 Dec 2021 09:15:32 GMT  
		Size: 196.4 KB (196434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4350870c5032cb99dc340de3b03f34f6c64551c582db28b9f98f3596393121`  
		Last Modified: Thu, 02 Dec 2021 09:15:32 GMT  
		Size: 958.7 KB (958661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d9339bbf2acc17dbede0642b1eafe30f032e1315d3f4b82349f11664b8db34b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.0 MB (434027305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ac9b007840ee26aeed58315aa41963fcc0584c80fd8252f3ac7eecb5416aad`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:45:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 02:46:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:48:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 00:58:08 GMT
ENV OTP_VERSION=24.1.7 REBAR3_VERSION=3.17.0
# Tue, 23 Nov 2021 00:58:08 GMT
LABEL org.opencontainers.image.version=24.1.7
# Tue, 23 Nov 2021 01:08:35 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1dd1a238f1f3e79784b902f3cd00e06f35a630191eaf73324a07a26a2c93af3" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 23 Nov 2021 01:08:36 GMT
CMD ["erl"]
# Tue, 23 Nov 2021 01:08:37 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 23 Nov 2021 01:08:46 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Tue, 23 Nov 2021 01:09:30 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9604eb6c465f658d6422593d504030155029fe0c4302451d4369030c29144`  
		Last Modified: Wed, 17 Nov 2021 03:07:14 GMT  
		Size: 7.1 MB (7125194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043b954c4f0757e89df96897cea2cf1f93c6275466008e4ba7a4b1089c7dd3d`  
		Last Modified: Wed, 17 Nov 2021 03:07:15 GMT  
		Size: 9.3 MB (9343839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf41461745fd89900c4b7cc794c93de081420bd83223b46e1495ff96748685c`  
		Last Modified: Wed, 17 Nov 2021 03:07:59 GMT  
		Size: 47.4 MB (47356485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4cebe2126c416f6186078f6b19742a166f0d535016a910ed5bd1bed73ab5ab`  
		Last Modified: Wed, 17 Nov 2021 03:09:46 GMT  
		Size: 168.6 MB (168608094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a67afd35aee5cd383d4eb2312323a9dd78892cb5edcd6efd5b00101a36d117`  
		Last Modified: Tue, 23 Nov 2021 01:36:04 GMT  
		Size: 154.5 MB (154520418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c480202e9c1755be43ec6d2ffc6cd04f8f48e4aae3bc2d6097abee1f77eb95c`  
		Last Modified: Tue, 23 Nov 2021 01:34:36 GMT  
		Size: 196.5 KB (196513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788f53347277b93191e46de05c6ddeaecf7f0735b4538e7bb09aa76b3bfdef49`  
		Last Modified: Tue, 23 Nov 2021 01:34:36 GMT  
		Size: 958.7 KB (958663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:dde836964733b25a8be72517641d06f6af826d953ffb878c92f53bd5c8784919
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.9 MB (463857031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19ec90fe73854510e4c5c3e9398effe3e0227dbbadd82a0b5beb06ab1aaa980`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 13:28:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:29:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 00:39:40 GMT
ENV OTP_VERSION=24.1.7 REBAR3_VERSION=3.17.0
# Tue, 23 Nov 2021 00:39:41 GMT
LABEL org.opencontainers.image.version=24.1.7
# Tue, 23 Nov 2021 00:44:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1dd1a238f1f3e79784b902f3cd00e06f35a630191eaf73324a07a26a2c93af3" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 23 Nov 2021 00:44:59 GMT
CMD ["erl"]
# Tue, 23 Nov 2021 00:45:01 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 23 Nov 2021 00:45:06 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Tue, 23 Nov 2021 00:45:31 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7f2500f9574b0a495bfb031c2d52e83c96dd545ef2185737f8032567e70677`  
		Last Modified: Wed, 17 Nov 2021 13:38:03 GMT  
		Size: 52.2 MB (52165947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16922d4fa4f2c649c56a586e06135309b0cc7e160a17c909e5eb349988df61aa`  
		Last Modified: Wed, 17 Nov 2021 13:38:38 GMT  
		Size: 184.0 MB (183991560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ee9d5754022c2f4107e9eb256292c7241475f1259ae92c8c0f40d7a6acac69`  
		Last Modified: Tue, 23 Nov 2021 00:58:14 GMT  
		Size: 159.9 MB (159859263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58098a495d98117782c58b59e5a464ab0d0e5c9c4f60a396d0c12293a7342f3f`  
		Last Modified: Tue, 23 Nov 2021 00:57:48 GMT  
		Size: 196.4 KB (196413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4c65e8c8d68328be4cf73c6faa6e21f8f60cf379d8b7b9723f9ffd95394872`  
		Last Modified: Tue, 23 Nov 2021 00:57:48 GMT  
		Size: 958.6 KB (958564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; 386

```console
$ docker pull erlang@sha256:fc8d0f08312642ce718c6837d2745083f9be9bb4d59b53f25b203fadc161f85e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488677098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9f743e7af18a4ca0555fe36062c0522b861aae2be068b0f02c8dc97d786a0a`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 02 Dec 2021 02:40:08 GMT
ADD file:bc6354e2db2c2d7e91d408526595618af60bda4ed24c3669f5cea44654246a02 in / 
# Thu, 02 Dec 2021 02:40:09 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:12:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:12:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:12:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:14:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:27:21 GMT
ENV OTP_VERSION=24.1.7 REBAR3_VERSION=3.17.0
# Thu, 02 Dec 2021 03:27:21 GMT
LABEL org.opencontainers.image.version=24.1.7
# Thu, 02 Dec 2021 03:42:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1dd1a238f1f3e79784b902f3cd00e06f35a630191eaf73324a07a26a2c93af3" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:42:03 GMT
CMD ["erl"]
# Thu, 02 Dec 2021 03:42:03 GMT
ENV REBAR_VERSION=2.6.4
# Thu, 02 Dec 2021 03:42:09 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Thu, 02 Dec 2021 03:42:40 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:3ed3f8c8d2c596bcef8beee90c4666003f0848cc4a23aaa9a695092c1c5da63e`  
		Last Modified: Thu, 02 Dec 2021 02:48:30 GMT  
		Size: 51.2 MB (51207683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a877cd82b20bae956837093ebe6cd6e2c60e19eb18d865d0bacad7eb5b9f97c`  
		Last Modified: Thu, 02 Dec 2021 03:22:15 GMT  
		Size: 8.0 MB (8000230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5f6e3cfc04d16a83c90de99f5d4214b99409d72c73084aea9d8974d23ac0ce`  
		Last Modified: Thu, 02 Dec 2021 03:22:15 GMT  
		Size: 10.3 MB (10340119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325cedb9579adc79c47e946667557b202cffac402c38f76e9e879a8f4ca2469d`  
		Last Modified: Thu, 02 Dec 2021 03:22:40 GMT  
		Size: 53.4 MB (53438254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27671a9182184c838f54d26bca25193b0e724abbdde607bb497bd9f7e6417002`  
		Last Modified: Thu, 02 Dec 2021 03:23:30 GMT  
		Size: 199.0 MB (198961872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fa137c50524618b1c65c81748448ea516598e46070511272ed64f9b8d50484`  
		Last Modified: Thu, 02 Dec 2021 08:35:43 GMT  
		Size: 165.6 MB (165573861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a48a4afef2c10168f9f344cd7ba89c767d144a3fa9dcbf3c1e902d59863d69`  
		Last Modified: Thu, 02 Dec 2021 08:34:47 GMT  
		Size: 196.4 KB (196418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5176a4b21909371de90724f61b466f043f75aa7bb2baf0ae4ed4f2b096a3f45`  
		Last Modified: Thu, 02 Dec 2021 08:34:47 GMT  
		Size: 958.7 KB (958661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; ppc64le

```console
$ docker pull erlang@sha256:871c6261db4543011167921e40a3a950efab68b8dbdcfa1ff3f0d8a61b59be2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.1 MB (503077625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c13f222acf807c2aa0cf0e727945c6aad0dc880b6b617b82849cd7a57ee32b7`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Nov 2021 03:29:10 GMT
ADD file:fc0d43ba74311deef20b2131cca3a8e86b083624d63560251191adca21417f2f in / 
# Wed, 17 Nov 2021 03:29:20 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 07:52:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 07:53:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 07:55:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 08:06:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 01:16:32 GMT
ENV OTP_VERSION=24.1.7 REBAR3_VERSION=3.17.0
# Tue, 23 Nov 2021 01:16:33 GMT
LABEL org.opencontainers.image.version=24.1.7
# Tue, 23 Nov 2021 01:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1dd1a238f1f3e79784b902f3cd00e06f35a630191eaf73324a07a26a2c93af3" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 23 Nov 2021 01:28:17 GMT
CMD ["erl"]
# Tue, 23 Nov 2021 01:28:19 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 23 Nov 2021 01:28:29 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Tue, 23 Nov 2021 01:29:12 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:aad6e1fe6f7c56b0e1b5850f40e4fec91ffaed4b6235e730f5c7ff43db397d3d`  
		Last Modified: Wed, 17 Nov 2021 03:56:39 GMT  
		Size: 54.2 MB (54183702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38c773e3945e9939b7299519ac8a7f3ad909af69c2d7291d8dfb6e7fa6eccfe`  
		Last Modified: Wed, 17 Nov 2021 08:28:50 GMT  
		Size: 8.3 MB (8272985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e0d54cc06e26d154b6f6e9746c8de2af93d9f635c280336663372f382fcd46`  
		Last Modified: Wed, 17 Nov 2021 08:28:49 GMT  
		Size: 10.7 MB (10727776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3239f513a520f7d81f241b123128d80a0c91d3ef8697270ffae67898934cb4f9`  
		Last Modified: Wed, 17 Nov 2021 08:29:36 GMT  
		Size: 57.5 MB (57457385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f80735649ead4029d67b9d28dac87b66bb06e2548f5c0d68c5f9877855d41c`  
		Last Modified: Wed, 17 Nov 2021 08:31:23 GMT  
		Size: 203.3 MB (203301921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874c6c87176425bc142c45f71f11ef3d66769aacc1090b826a14c24d978e4fca`  
		Last Modified: Tue, 23 Nov 2021 01:47:44 GMT  
		Size: 168.0 MB (167978679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7150e436265b245f51cede4cb95f9ec4a1509ba96b37616c0ea2ff1ee25a52`  
		Last Modified: Tue, 23 Nov 2021 01:47:16 GMT  
		Size: 196.5 KB (196518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9d7c8dca3ee641133e348e1c69405508f8e86df704d541325ff3195b23394e`  
		Last Modified: Tue, 23 Nov 2021 01:47:17 GMT  
		Size: 958.7 KB (958659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:latest` - linux; s390x

```console
$ docker pull erlang@sha256:37f2675dc6e01a14bc7d8c3c82e715ff141784610c9d97630a1e8e3cbb23882d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.0 MB (456968386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85a69b9ee91ee96c0e0af956c4efbcc3218de2a02da5a2ab0170a91e0494ed9`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:40 GMT
ADD file:dc4ee96f81059accdc88a686f80f1714bc9d2f383af71c0d130c08560cea115e in / 
# Wed, 17 Nov 2021 02:42:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:10:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:10:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 03:10:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:11:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 00:41:31 GMT
ENV OTP_VERSION=24.1.7 REBAR3_VERSION=3.17.0
# Tue, 23 Nov 2021 00:41:31 GMT
LABEL org.opencontainers.image.version=24.1.7
# Tue, 23 Nov 2021 00:46:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="a1dd1a238f1f3e79784b902f3cd00e06f35a630191eaf73324a07a26a2c93af3" 	&& runtimeDeps='libodbc1 			libsctp1 			libwxgtk3.0' 	&& buildDeps='unixodbc-dev 			libsctp-dev 			libwxgtk3.0-dev' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make -j$(nproc) docs DOC_TARGETS=chunks 	  && make install install-docs DOC_TARGETS=chunks ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 23 Nov 2021 00:47:03 GMT
CMD ["erl"]
# Tue, 23 Nov 2021 00:47:03 GMT
ENV REBAR_VERSION=2.6.4
# Tue, 23 Nov 2021 00:47:12 GMT
RUN set -xe 	&& REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" 	&& REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" 	&& mkdir -p /usr/src/rebar-src 	&& curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" 	&& echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 	&& rm rebar-src.tar.gz 	&& cd /usr/src/rebar-src 	&& ./bootstrap 	&& install -v ./rebar /usr/local/bin/ 	&& rm -rf /usr/src/rebar-src
# Tue, 23 Nov 2021 00:47:28 GMT
RUN set -xe 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="4c7f33a342bcab498f9bf53cc0ee5b698d9598b8fa9ef6a14bcdf44d21945c27" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src
```

-	Layers:
	-	`sha256:c12eae84d2674466d924a139a276e361afa9f63de21cf77eae19bd94eaac2629`  
		Last Modified: Wed, 17 Nov 2021 02:48:42 GMT  
		Size: 49.0 MB (49005439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a8b4bf4cf08933f04084cd556e9c716474b9801854ea7c4473c9804894516`  
		Last Modified: Wed, 17 Nov 2021 03:18:14 GMT  
		Size: 7.4 MB (7401273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffdc4b0bb501f5f5214892baa1a5d53d44ce92b645995a43fe2cfeb2ffec6d1`  
		Last Modified: Wed, 17 Nov 2021 03:18:14 GMT  
		Size: 9.9 MB (9883156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb48942b4b14ee80905b23bc6babae28a961847a914becfe41686d368d8693d`  
		Last Modified: Wed, 17 Nov 2021 03:18:28 GMT  
		Size: 51.4 MB (51380227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deaef082aa42f5164fd0beb9cf445ba4867c9ad41c784080a427bc615a02df9`  
		Last Modified: Wed, 17 Nov 2021 03:18:54 GMT  
		Size: 176.9 MB (176912713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a1ba02b1d23cd9a0bd053ae7f34d53043adcff08976d0ea20aa24a3119b252`  
		Last Modified: Tue, 23 Nov 2021 00:58:10 GMT  
		Size: 161.2 MB (161230413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cedda7f913cec97257a3f7b7bcd3c643528c746ccbf0ce74eb96e8005cbba3`  
		Last Modified: Tue, 23 Nov 2021 00:57:52 GMT  
		Size: 196.5 KB (196511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfe5d4332753f10d8b0138df5af25970789b1e343a2c74e377ac92a47737b3e`  
		Last Modified: Tue, 23 Nov 2021 00:57:52 GMT  
		Size: 958.7 KB (958654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
