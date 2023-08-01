## `perl:devel`

```console
$ docker pull perl@sha256:edc71b617241310029e1ede72986e5e496292514adcf3a0db497b2dc13227176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:devel` - linux; amd64

```console
$ docker pull perl@sha256:ad2ac0e62e0ddf6dcadb140ea3ed9ea31c53db845df2809cb274d442fb7fd9e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.4 MB (364386740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce82b6071e95b25a91094d75bb054678125b99ef6ba3e0daefd44f572cad2a1`
-	Default Command: `["perl5.39.1","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:29 GMT
ADD file:cc1376ecb3d9e93e4160573c110da753ffeb2efe2223351f1fbf483d89f1a756 in / 
# Thu, 27 Jul 2023 23:24:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:00:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:01:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:02:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:44:20 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 06:44:20 GMT
WORKDIR /usr/src/perl
# Tue, 01 Aug 2023 02:30:14 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.39.1.tar.xz -o perl-5.39.1.tar.xz     && echo '326b797eb65946026c932f1750d740e908566c5c7e847341e1d60f63324fd03e *perl-5.39.1.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.1.tar.xz -C /usr/src/perl     && rm perl-5.39.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Tue, 01 Aug 2023 02:30:14 GMT
WORKDIR /
# Tue, 01 Aug 2023 02:30:14 GMT
CMD ["perl5.39.1" "-de0"]
```

-	Layers:
	-	`sha256:785ef8b9b236a5f027f33cae77513051704c0538bff455ff5548105c954c3b1c`  
		Last Modified: Thu, 27 Jul 2023 23:29:02 GMT  
		Size: 49.6 MB (49557354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6dad8f55ae6c733e986316bd08205c8b2c41640bf8d08ff6e9bbcb6884304f`  
		Last Modified: Fri, 28 Jul 2023 03:07:18 GMT  
		Size: 24.0 MB (24030539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd36c7bfe5f4bdffcc0bbb74b0fb38feb35c286ea58b5992617fb38b0c933603`  
		Last Modified: Fri, 28 Jul 2023 03:07:36 GMT  
		Size: 64.1 MB (64112293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d207285f6d296b9806bd00340437406c25207412c52fcfcbf229a5ecff7bf94`  
		Last Modified: Fri, 28 Jul 2023 03:08:11 GMT  
		Size: 211.0 MB (211031643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b86e0a75d1f09ded7102407f86f6ab03cbadc1239010c3a9a23bc4cb7a0c53`  
		Last Modified: Fri, 28 Jul 2023 10:34:23 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e6a2cd8695f3a5ad9c896e2a8b205994a48661e3513362c730de06874795cf`  
		Last Modified: Tue, 01 Aug 2023 03:22:29 GMT  
		Size: 15.7 MB (15654744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel` - linux; arm variant v7

```console
$ docker pull perl@sha256:f1b042917e88cb97a12830dcced38c41d25bb9325db16ee68431501f785def29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297487741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779e7a0b342203c8dfef14587c8547717ce85ac4e88cd81e7f002db3b70fe441`
-	Default Command: `["perl5.37.11","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:58:01 GMT
ADD file:3014d2ee0e0e882151b5295faeb81a24b4d6f9e0f92f3ba969ccffb2bd8a6d76 in / 
# Thu, 27 Jul 2023 23:58:03 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:59:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:01:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 07:12:43 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 07:12:43 GMT
WORKDIR /usr/src/perl
# Fri, 28 Jul 2023 10:25:47 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.11.tar.xz -o perl-5.37.11.tar.xz     && echo '3946b00266595ccc44df28275e2fbb7b86c1482934cbeab2780db304a75ffd58 *perl-5.37.11.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.11.tar.xz -C /usr/src/perl     && rm perl-5.37.11.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Fri, 28 Jul 2023 10:25:47 GMT
WORKDIR /
# Fri, 28 Jul 2023 10:25:47 GMT
CMD ["perl5.37.11" "-de0"]
```

-	Layers:
	-	`sha256:e8dff7ada2c26d71087c5ec6294d1adc4dcf7d688824a079e89e3bedd9a34fa6`  
		Last Modified: Fri, 28 Jul 2023 00:03:32 GMT  
		Size: 50.2 MB (50218549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa87808c3418d080808a65b8798629209aa23ef6dd21a2495b3d99e8367242`  
		Last Modified: Fri, 28 Jul 2023 02:07:34 GMT  
		Size: 14.9 MB (14868822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017eba29227541589419d3d28eb04fefe86aa7fa5ec809386432bedd612c979f`  
		Last Modified: Fri, 28 Jul 2023 02:07:51 GMT  
		Size: 50.4 MB (50355308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6945de828a2eb1ee480a75a3c86b584d5eb7eb1d37bca07eccd5052961c49d`  
		Last Modified: Fri, 28 Jul 2023 02:08:20 GMT  
		Size: 167.3 MB (167332243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695665838fd809fc7d7dca28c0096b165fe64c37e2aa43a642d3602d7e3d5f98`  
		Last Modified: Fri, 28 Jul 2023 11:09:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef5c97436f6b92f5ede441b75fe47f6e6d1e9aeb36be82a30a15f1a8820ff7f`  
		Last Modified: Fri, 28 Jul 2023 11:17:45 GMT  
		Size: 14.7 MB (14712651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:49ef050cf5fba6676939525dedd69ad130cd35bed9482c5b571c02b9f43bee93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355190794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7382780fa4d4a959234b856b920da7047560305d0d28498566a3b6fc1f189652`
-	Default Command: `["perl5.39.1","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:42:51 GMT
ADD file:fa545fc37115e874135945921d2cc72df8dc5b16d4354b2052717c7a57043e0d in / 
# Thu, 27 Jul 2023 23:42:51 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:35:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:36:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:37:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:42:32 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 06:42:32 GMT
WORKDIR /usr/src/perl
# Tue, 01 Aug 2023 02:20:37 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.39.1.tar.xz -o perl-5.39.1.tar.xz     && echo '326b797eb65946026c932f1750d740e908566c5c7e847341e1d60f63324fd03e *perl-5.39.1.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.1.tar.xz -C /usr/src/perl     && rm perl-5.39.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Tue, 01 Aug 2023 02:20:37 GMT
WORKDIR /
# Tue, 01 Aug 2023 02:20:37 GMT
CMD ["perl5.39.1" "-de0"]
```

-	Layers:
	-	`sha256:fc9ce7290e7e014f69623715ba619a0d3488a7b6ecbf09e55e11160365691192`  
		Last Modified: Thu, 27 Jul 2023 23:45:54 GMT  
		Size: 49.6 MB (49591268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73373011d63f722a4ac6bc23ce7831a17f19e27ef530544642f060aa1d6b028b`  
		Last Modified: Fri, 28 Jul 2023 01:41:58 GMT  
		Size: 23.6 MB (23570127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dafffb02e2671e7e5cc07c996fed89f6ccc8e3276ce2dc1bbfb81502cdd795`  
		Last Modified: Fri, 28 Jul 2023 01:42:15 GMT  
		Size: 64.0 MB (63988301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cd1c60bb2c0a9bd6653d88494ac5f855634c2ec64a14cfa547ab2e257c6519`  
		Last Modified: Fri, 28 Jul 2023 01:42:45 GMT  
		Size: 202.4 MB (202421010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413acd89fecae00634847cd8ba73940b4aa1ee9358b38f1ead4d2c1922fffe4b`  
		Last Modified: Fri, 28 Jul 2023 09:52:24 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69deecb0994117d51d1483c511c70e1c1bfd2c970ff552246d4d4953d2bc683e`  
		Last Modified: Tue, 01 Aug 2023 03:05:37 GMT  
		Size: 15.6 MB (15619921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel` - linux; 386

```console
$ docker pull perl@sha256:297b0ec0a4cfd70033100787a11620d495e957f728f06eac3b6d9c61afc5af07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343116084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e12165146a5187f1040dd8f0fc962eafa741898eeddd5576580b5d460399848`
-	Default Command: `["perl5.37.11","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:07 GMT
ADD file:6ae90664cb71d88535d2be8e87b3a14dadaa5dad7756db4b7c26638d53c55187 in / 
# Thu, 27 Jul 2023 23:39:08 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 09:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 09:05:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 09:06:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jul 2023 00:35:16 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Sat, 29 Jul 2023 00:35:16 GMT
WORKDIR /usr/src/perl
# Sat, 29 Jul 2023 03:09:19 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.11.tar.xz -o perl-5.37.11.tar.xz     && echo '3946b00266595ccc44df28275e2fbb7b86c1482934cbeab2780db304a75ffd58 *perl-5.37.11.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.11.tar.xz -C /usr/src/perl     && rm perl-5.37.11.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Sat, 29 Jul 2023 03:09:19 GMT
WORKDIR /
# Sat, 29 Jul 2023 03:09:19 GMT
CMD ["perl5.37.11" "-de0"]
```

-	Layers:
	-	`sha256:8de74d843a460b113b2683caf2d7e61b9d0ed2575871f77b575c62d4244922f7`  
		Last Modified: Thu, 27 Jul 2023 23:43:47 GMT  
		Size: 56.0 MB (56040964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbaaf1649176f88d4a59e288aaf81eb04629cf22fa6084af27a43d2d019af413`  
		Last Modified: Fri, 28 Jul 2023 09:12:21 GMT  
		Size: 16.3 MB (16263799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3677802a52382b7234476219d1b0ea7381578cfe46772a2d48061d57d941103a`  
		Last Modified: Fri, 28 Jul 2023 09:12:41 GMT  
		Size: 55.9 MB (55923050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1621baec8fbfa542b43791bd697b85a8e5e967ea7f9baf0b11f47951cd9b949d`  
		Last Modified: Fri, 28 Jul 2023 09:13:23 GMT  
		Size: 199.8 MB (199767498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338cf4d5c0b9957bda14b209de4598a262b086a6a8bcfe6b94097c94d3c66680`  
		Last Modified: Sat, 29 Jul 2023 03:40:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ac57a11ca1ec5bac8580dce7addf216090bec920502ecc4dd4d1036e304e7a`  
		Last Modified: Sat, 29 Jul 2023 03:44:27 GMT  
		Size: 15.1 MB (15120605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
