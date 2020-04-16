## `perl:5-threaded-stretch`

```console
$ docker pull perl@sha256:47d561befcd42c9c75f744ff860d086f3ff7ec516bf4c7b15bf225e4ab259b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `perl:5-threaded-stretch` - linux; amd64

```console
$ docker pull perl@sha256:338bcc6f68f2fef2304d0f73fdbb79756a01427e0a0c94a5a865a381eb61835d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339360174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97059eecac6eccf48a85450725f2c685d969d6ef06514fcce9dbb5fced7c906e`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 02:07:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:08:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:53:26 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 31 Mar 2020 08:53:27 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Tue, 31 Mar 2020 08:53:27 GMT
WORKDIR /usr/src/perl
# Tue, 31 Mar 2020 09:59:59 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 31 Mar 2020 09:59:59 GMT
WORKDIR /
# Tue, 31 Mar 2020 10:00:00 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e1e13bd9f6c381f158a5366b3eff242e8b4a4decfa940e915b1d5705ef4a28`  
		Last Modified: Tue, 31 Mar 2020 02:12:58 GMT  
		Size: 50.1 MB (50071604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86b38b40a24c042077b816eebfc5356bf938c6aed3069e102175ef1720416b8`  
		Last Modified: Tue, 31 Mar 2020 02:13:37 GMT  
		Size: 214.9 MB (214906068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f53e6370ec49bdbaa334892ec53ccccea0a1de71707fb2974fde3a9185ed8d4`  
		Last Modified: Tue, 31 Mar 2020 13:16:39 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ece96ce5eb61c6c80e65796d277c739ad5b8efdf1238b301463ce177dc8ea1`  
		Last Modified: Tue, 31 Mar 2020 13:17:35 GMT  
		Size: 13.9 MB (13868717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-stretch` - linux; arm variant v7

```console
$ docker pull perl@sha256:dae8f5c2ea199246e63232f98ab797a4b8058380587c7c5933034d66c0f75b89
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310488512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae3e653728d61fb1d4014add5036ab54bc8d4df9148a65816732e1cbd9b3b1f`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 01:04:37 GMT
ADD file:b83ed4f9f7c8b10eba728f85030722a771b39336afd7ff9eef2eb6b94791533e in / 
# Thu, 16 Apr 2020 01:04:40 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:50:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:50:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 01:51:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:53:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 05:36:12 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 05:36:12 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 05:36:13 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 06:35:45 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 06:35:48 GMT
WORKDIR /
# Thu, 16 Apr 2020 06:35:48 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:37d8a5aac9ec54f7757e1243cff051c8372be0cf907e086fba2607e08d2a4135`  
		Last Modified: Thu, 16 Apr 2020 01:12:16 GMT  
		Size: 42.1 MB (42101227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f4f4abba4245745ee86a35473696f5ecbe961a03af35bd6f07b2253c3bedba`  
		Last Modified: Thu, 16 Apr 2020 01:59:44 GMT  
		Size: 9.5 MB (9498336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3accf104e4ac412a36f3c1fc31fb94722661bf356ac878a4b502dc20086c8d2f`  
		Last Modified: Thu, 16 Apr 2020 01:59:42 GMT  
		Size: 3.9 MB (3918841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b661b06bea35fef2d1bfd84e8d9bb0f243557b3d08139187ad1d0956db6fccc0`  
		Last Modified: Thu, 16 Apr 2020 02:00:05 GMT  
		Size: 46.4 MB (46410934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfd73fcb2a87267ab0f0d969574064aa6b804681b72b3642486b35336335d3e`  
		Last Modified: Thu, 16 Apr 2020 02:01:03 GMT  
		Size: 195.6 MB (195565244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9094588a67f2567b2988727ade552537b7023cae340f827b08b52f5763c1c189`  
		Last Modified: Thu, 16 Apr 2020 09:46:27 GMT  
		Size: 441.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042c15132a967d49c7e3e76a1cca71e9437b48b13e03c8710bc5535ff61af5e2`  
		Last Modified: Thu, 16 Apr 2020 09:47:36 GMT  
		Size: 13.0 MB (12993489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-stretch` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:a078d712f49b0e5f8358fd8ebd03b975a6ebe1174530e6ee30ee191acd74b600
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320985018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f9bdf33a8a8e0d3ee905dcfd9402dbada553e7de220d7e9f2fabcec3d58c9d`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 04:42:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:44:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 09:37:06 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 31 Mar 2020 09:37:07 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Tue, 31 Mar 2020 09:37:08 GMT
WORKDIR /usr/src/perl
# Tue, 31 Mar 2020 10:31:09 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 31 Mar 2020 10:31:10 GMT
WORKDIR /
# Tue, 31 Mar 2020 10:31:11 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4110ff81d02419c6737ebf46680f0afee475f58cf3bd159e0892d8f4ffebaf`  
		Last Modified: Tue, 31 Mar 2020 04:50:00 GMT  
		Size: 48.0 MB (48024387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e867f7ebdcf1b584d20b2d8a16d449dd728ce0d4cab78f8f46e281cc1c371aab`  
		Last Modified: Tue, 31 Mar 2020 04:51:02 GMT  
		Size: 202.3 MB (202281623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c830469b54b1138075ad9eee06a74f8e1fa2ea7d4f7902b74ca4cd40a8f13bd`  
		Last Modified: Tue, 31 Mar 2020 13:55:05 GMT  
		Size: 442.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71283557c18676871f7be9123d442ddb5779eb40dfe58b838fa748ccdccf661e`  
		Last Modified: Tue, 31 Mar 2020 13:56:14 GMT  
		Size: 13.7 MB (13677593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-stretch` - linux; 386

```console
$ docker pull perl@sha256:b2f3326fbce464f6a892b2af37ea9405d14155056678bbaafb9ced16b112113c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346434221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2674f5463e2a44dff2ae36b5486e2a1473fa94dc4ace83c2aa3c333f47646be`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Tue, 31 Mar 2020 00:42:34 GMT
ADD file:a2d15d4f5721611194d2e75c068cf76220a1fd273b28e60afc9d97c41920f37b in / 
# Tue, 31 Mar 2020 00:42:34 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:25:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:25:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:25:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:26:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 06:15:23 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 31 Mar 2020 06:15:23 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Tue, 31 Mar 2020 06:15:24 GMT
WORKDIR /usr/src/perl
# Tue, 31 Mar 2020 07:31:41 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 31 Mar 2020 07:31:41 GMT
WORKDIR /
# Tue, 31 Mar 2020 07:31:42 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:e23f42c0de4ea650702adc216b9d71349a24439e774c0bbbb00d2ad19aa304df`  
		Last Modified: Tue, 31 Mar 2020 00:48:31 GMT  
		Size: 46.1 MB (46095182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a8aed54eafba002eda33cfdc543523b6ddb486d1a0cbca690ff815f53d50e9`  
		Last Modified: Tue, 31 Mar 2020 01:32:58 GMT  
		Size: 10.8 MB (10818153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a1db665f4b770126afb4ccdc427fae19617bf624b95982ce876d0fdb478291`  
		Last Modified: Tue, 31 Mar 2020 01:32:56 GMT  
		Size: 4.6 MB (4561461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b716c001feda21116c3228663db9da4551f266d173d7526106f39b3c53d27212`  
		Last Modified: Tue, 31 Mar 2020 01:33:17 GMT  
		Size: 51.6 MB (51603799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b641c40e42054609b087ee068d26211f8add45c247766ce2aa069bcb8a8dcce7`  
		Last Modified: Tue, 31 Mar 2020 01:34:18 GMT  
		Size: 220.0 MB (219957071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76353b54f8f72462453fe61bc20e582db0dd8b638fc8dcdd48d83e56dde7ead7`  
		Last Modified: Tue, 31 Mar 2020 11:32:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501e662157a63a8123ca96ea593f564283076f97a73a0c9a20899101887106f9`  
		Last Modified: Tue, 31 Mar 2020 11:33:30 GMT  
		Size: 13.4 MB (13398138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-stretch` - linux; ppc64le

```console
$ docker pull perl@sha256:bae9ea01a9e490cecc5495e1a7b28d999e5a3d8143a5b7c63d548ba1e81b26ec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334303233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fa51d4ab475d11fadc4f73fc10ec2cd83935e666cf2c97068631f290a302cd`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Tue, 31 Mar 2020 01:36:08 GMT
ADD file:88dd9829c8f6a5ba7164ab347e4b14c986122f77fa3881b5b5f9bd34f8e0a794 in / 
# Tue, 31 Mar 2020 01:36:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:46:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:46:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 03:48:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:56:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 07:47:09 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 31 Mar 2020 07:47:10 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Tue, 31 Mar 2020 07:47:12 GMT
WORKDIR /usr/src/perl
# Tue, 31 Mar 2020 08:27:38 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 31 Mar 2020 08:27:50 GMT
WORKDIR /
# Tue, 31 Mar 2020 08:27:56 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:a7f28865f7aedbe572d508cc57c37cad5f147864f7c67c67a38458e070687420`  
		Last Modified: Tue, 31 Mar 2020 01:52:56 GMT  
		Size: 45.6 MB (45647140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b575341a09a9b1fed08dca01f194be6db272e3f2d161ea2edf0db64d8e706213`  
		Last Modified: Tue, 31 Mar 2020 04:07:20 GMT  
		Size: 10.0 MB (10002319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28423de192fc0e4ecfc04a57e531587e8876d098a124122748a8f55a842f3213`  
		Last Modified: Tue, 31 Mar 2020 04:07:19 GMT  
		Size: 4.3 MB (4296673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cccdb86da25ba4684a518e5fe94d237bd1d84392cdee077d26f6aed0520237e`  
		Last Modified: Tue, 31 Mar 2020 04:08:09 GMT  
		Size: 50.1 MB (50085204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe17ae7a3b975904e86d12aae11a52d1775c818c61d0513cbfaa36fa3ad4352`  
		Last Modified: Tue, 31 Mar 2020 04:09:18 GMT  
		Size: 210.5 MB (210525053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a28a55ab968e10a98494850d9a9d360a3bb0902deb99aa3628f425161bfb72`  
		Last Modified: Tue, 31 Mar 2020 10:48:08 GMT  
		Size: 443.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ddb175b7f2ff7af7720e37430f69f11062c8c4ab409899db262db5a8c49e17`  
		Last Modified: Tue, 31 Mar 2020 10:49:52 GMT  
		Size: 13.7 MB (13746401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-stretch` - linux; s390x

```console
$ docker pull perl@sha256:5410f0b75b36d1f8da731eb1b5fafe6ace3d74ec4261462a31ec702af81b513f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331657303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2ab0e0742a47f68100efb8105104d32000bdd681a8f5e488253e977456c597`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 00:43:47 GMT
ADD file:bf54e49d85edbe8d61bd9e868d71faf0f26b4474f23eda7b692abfaf7aea50a4 in / 
# Thu, 16 Apr 2020 00:43:49 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:02:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 02:03:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:04:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:35:43 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 03:35:43 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 03:35:43 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 03:59:41 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 03:59:42 GMT
WORKDIR /
# Thu, 16 Apr 2020 03:59:43 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:b4e6598a8ad88c3d661d89d6fda41ee33a54f3c6f16c4988cceaa6fd0afd04bb`  
		Last Modified: Thu, 16 Apr 2020 00:48:18 GMT  
		Size: 45.2 MB (45232626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cb98b0a4ec56e95b4ba3f3261ba975cd69e2a0240149eb53e4bbff9739e272`  
		Last Modified: Thu, 16 Apr 2020 02:08:04 GMT  
		Size: 10.3 MB (10325610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c82c0f221bc14891b71387b7587fd4f2a615d339ecf0afadce350f82b3e098`  
		Last Modified: Thu, 16 Apr 2020 02:08:03 GMT  
		Size: 4.4 MB (4372651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d17818ca9e172b803a01ef9860f9b1c67b359a6d75c51e65a63c0448b3816d`  
		Last Modified: Thu, 16 Apr 2020 02:08:18 GMT  
		Size: 50.5 MB (50513161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2557aea605e0656c02d9c1b5edabffb8913484720675da14238c640088e5999`  
		Last Modified: Thu, 16 Apr 2020 02:08:56 GMT  
		Size: 206.9 MB (206917991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21003175356a3d83c170d92cd0049cd7768b36cc178dea3254d08fe227e8b8f8`  
		Last Modified: Thu, 16 Apr 2020 05:23:15 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163eedfd509f0573f0aa2e34f20e64bc64ef56a19a31416a3dade805ab038cb5`  
		Last Modified: Thu, 16 Apr 2020 05:24:06 GMT  
		Size: 14.3 MB (14294825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
