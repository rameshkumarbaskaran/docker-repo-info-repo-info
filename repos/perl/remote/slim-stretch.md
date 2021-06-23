## `perl:slim-stretch`

```console
$ docker pull perl@sha256:54b4a10b91d467a5274e439807307a39e01a7fa06d6fea16e1c917a4b166fa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:slim-stretch` - linux; amd64

```console
$ docker pull perl@sha256:1ebb3ee64d03bb0aabd8e432858412d98a046ae84f9da3293307a93638961cfb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37119847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d6afaa86014b94c32c6b59f944dca4a250093abded1d48ee1a04b70f762985`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Wed, 12 May 2021 01:23:21 GMT
ADD file:a88164546613d1850e5c5494cccad7124d713187bfabf592a783eb9328de51eb in / 
# Wed, 12 May 2021 01:23:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 09:22:53 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 12 May 2021 09:22:53 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 12 May 2021 09:22:53 GMT
WORKDIR /usr/src/perl
# Wed, 12 May 2021 09:31:14 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 12 May 2021 09:31:14 GMT
WORKDIR /
# Wed, 12 May 2021 09:31:15 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:fa1690ae92289fb310aa27b793a164bf8bbedc7ddd00ca079a31bb8bb315b616`  
		Last Modified: Wed, 12 May 2021 01:30:20 GMT  
		Size: 22.5 MB (22528266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48268c9a1d0ee3d1f7d5fc0d5bf74be0a3e3182d2080440489e8d2a45eb4b0c4`  
		Last Modified: Wed, 12 May 2021 12:36:15 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2f473d41c3a92caac654ac128710696fde4fdd22d46cde9ae2b3a031d639e7`  
		Last Modified: Wed, 12 May 2021 12:36:19 GMT  
		Size: 14.6 MB (14591379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-stretch` - linux; arm variant v7

```console
$ docker pull perl@sha256:410ba0836f9e14b19460348f51d80e90437fd294193f9f72cc7e63841e43bd63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33046401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd9112dce6473f6856f56b8b70f03215c52d9dd74937401550481bd71c474b`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Wed, 12 May 2021 01:13:00 GMT
ADD file:3a0c44e2f78c31814d76ce91706cea345d424f8b49631a1e01dbfe768d244d48 in / 
# Wed, 12 May 2021 01:13:05 GMT
CMD ["bash"]
# Tue, 25 May 2021 23:46:49 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 25 May 2021 23:46:49 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 25 May 2021 23:46:49 GMT
WORKDIR /usr/src/perl
# Tue, 25 May 2021 23:54:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 25 May 2021 23:54:12 GMT
WORKDIR /
# Tue, 25 May 2021 23:54:13 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:ce2b35672977ffba9f48ce0726706cd15d926482c1008f69213433c61ba44966`  
		Last Modified: Wed, 12 May 2021 01:21:44 GMT  
		Size: 19.3 MB (19315154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa70a4b21f699ff4448b34723c3617c868df61d36986522d790c8a7312a05af1`  
		Last Modified: Wed, 26 May 2021 09:53:34 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a423745f07c20457df94fc3ebf9c25331e016ff021aa47c047337eb665f8d608`  
		Last Modified: Wed, 26 May 2021 09:53:38 GMT  
		Size: 13.7 MB (13731045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-stretch` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:1b7e2cb5ff12cc1f35c4d5e60acf79973f3a9fd1d36568cb14e3310cf1e54840
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34793545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5b426eb9f541b163f7502fb282285f0cf712f96b212dc4e47623d8a48707d8`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Tue, 22 Jun 2021 23:51:10 GMT
ADD file:0124cb1e13f08e2df3878b9faa69d962ba2b9c7d5afdf72fff8b1e22201ce065 in / 
# Tue, 22 Jun 2021 23:51:11 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 06:06:43 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 23 Jun 2021 06:06:43 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 23 Jun 2021 06:06:43 GMT
WORKDIR /usr/src/perl
# Wed, 23 Jun 2021 06:12:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 23 Jun 2021 06:12:41 GMT
WORKDIR /
# Wed, 23 Jun 2021 06:12:41 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:3ac59e1f301a0b03211a0a7f10a84730165b09211c4a8ef9636673101bf1220f`  
		Last Modified: Tue, 22 Jun 2021 23:58:21 GMT  
		Size: 20.4 MB (20389316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0b2687fc29cbd373243a53885acba10efc051eb2a00d4004847285b4230564`  
		Last Modified: Wed, 23 Jun 2021 07:36:00 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b0e9e37ed2e7fe9f0b0447b87dead4f63ca924f0132d09a14f1dafb6c4109e`  
		Last Modified: Wed, 23 Jun 2021 07:36:03 GMT  
		Size: 14.4 MB (14404027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-stretch` - linux; 386

```console
$ docker pull perl@sha256:bfb7c75dedc2e69b99227917dd1ac6f1923a6ce004f795c5f35c50c9f676c3f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37243537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391793bd033bed396b96a06a3efcd0dbcef2e4d449532fc545c54d2eea8af83f`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Wed, 12 May 2021 00:41:59 GMT
ADD file:1e77ef0444477c2378e1fe7ce2e0f741f1d571f4e165a55918634f5c982b2488 in / 
# Wed, 12 May 2021 00:41:59 GMT
CMD ["bash"]
# Wed, 12 May 2021 13:31:30 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 12 May 2021 13:31:30 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 12 May 2021 13:31:31 GMT
WORKDIR /usr/src/perl
# Wed, 12 May 2021 13:42:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 12 May 2021 13:42:06 GMT
WORKDIR /
# Wed, 12 May 2021 13:42:07 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:78aed7426e3ec56c5fe4bd663081f534a0389e8aaca5ef3373711f3172e64e0f`  
		Last Modified: Wed, 12 May 2021 00:49:44 GMT  
		Size: 23.2 MB (23156323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda24b76c491456d849e99a5843f5b4a940a045e105db644fe92f34599a985e6`  
		Last Modified: Wed, 12 May 2021 17:00:37 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd4a309c0d3365a84751282a5652a75ea5510b94ab058fce92f998728529834`  
		Last Modified: Wed, 12 May 2021 17:00:43 GMT  
		Size: 14.1 MB (14087013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
