## `perl:5-slim-threaded-buster`

```console
$ docker pull perl@sha256:e89be063676e1e5d821431042475c90bec80a381e9ac1ca390c6ee11de19999d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:5-slim-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:fdc1497bf27408c9537d5c23dcbbc25438925555fbc518dc0fbfafb84d815362
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54573037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a26adc3155161b6bdd907f91ded41bd904f5d20f0d8ef5084bd8342e24f4b5d`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:33 GMT
ADD file:29d3eb64d192a97184f2aa169407b58e969b06268c6372b49eefb72bcadb6e99 in / 
# Wed, 01 Nov 2023 00:21:34 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 08:07:38 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 01 Nov 2023 08:07:39 GMT
WORKDIR /usr/src/perl
# Wed, 01 Nov 2023 08:50:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 01 Nov 2023 08:50:46 GMT
WORKDIR /usr/src/app
# Wed, 01 Nov 2023 08:50:46 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:113c6ad4754853f4a2ae632cff7d90eba9145cca0bd6fa4d60aa432bd26be6c7`  
		Last Modified: Wed, 01 Nov 2023 00:26:56 GMT  
		Size: 27.2 MB (27187422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a5a78f49bc99358f4332458492c57417aa4e3e7dda0234198acc24984ebd44`  
		Last Modified: Wed, 01 Nov 2023 11:40:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a151388d5aaefe35b651b40ce93d74ebab01f3bb31016ad6f65105b3cb48e6c`  
		Last Modified: Wed, 01 Nov 2023 11:42:40 GMT  
		Size: 27.4 MB (27385283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7463116643340d64b76af4659e1fd9e0a4e893fddba1d1a14aa407cf832c87`  
		Last Modified: Wed, 01 Nov 2023 11:42:36 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:f141c4db52f589daeca5a9924ea2083521c91530249c081f3417bb3341ce8b2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46719089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a173a9d4f046cc5f3e98834f548e2cf95d78706f88d3b43c72e382b170de6e`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Wed, 01 Nov 2023 00:58:29 GMT
ADD file:dd923e222804a3bd200ecd72437d80c805c7eb6009aaa6b274da0574ccde56e0 in / 
# Wed, 01 Nov 2023 00:58:29 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 03:49:46 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 01 Nov 2023 03:49:46 GMT
WORKDIR /usr/src/perl
# Wed, 01 Nov 2023 04:32:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 01 Nov 2023 04:32:22 GMT
WORKDIR /usr/src/app
# Wed, 01 Nov 2023 04:32:22 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:43c30e0275ed5286753ad05a34be76f873205cce5130a05b3e968c87c888a5bf`  
		Last Modified: Wed, 01 Nov 2023 01:03:42 GMT  
		Size: 22.8 MB (22795940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b5ef21cc3a06a4e862f7348727cfceaee9a7faa45ae11f71954f46e4239946`  
		Last Modified: Wed, 01 Nov 2023 07:25:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3bd4f28901f5c9e215e20a3159882c7bfed0f20dd5adff21fbfa34ee31b677`  
		Last Modified: Wed, 01 Nov 2023 07:28:23 GMT  
		Size: 23.9 MB (23922815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda343de4f545abd0a7b25acb89271649c7f3aa0a8c9a463f71ffe770601cda3`  
		Last Modified: Wed, 01 Nov 2023 07:28:15 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:420d374f54f7d41a88c6523ec13a5382b46a156bac6f8bc188a4630daa8d69d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51960613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474bcb037c11caf8ceb801277c71484ee92809220d3950863f72610fadad0082`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:09 GMT
ADD file:ad1947b1fc97bcc228c004c15afeb2d9006d47167db69cf7b05c3e634c648166 in / 
# Wed, 01 Nov 2023 00:40:10 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 05:05:27 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 01 Nov 2023 05:05:27 GMT
WORKDIR /usr/src/perl
# Wed, 01 Nov 2023 05:39:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 01 Nov 2023 05:39:19 GMT
WORKDIR /usr/src/app
# Wed, 01 Nov 2023 05:39:19 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:094e0a7927f79c559fdab346774d7de6e5fc38e2d998e82dd663850ebbff4648`  
		Last Modified: Wed, 01 Nov 2023 00:44:25 GMT  
		Size: 26.0 MB (25967703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd48feab1145685f8b1a9b73d524444685a4266701e08ef6eb365d33619f041`  
		Last Modified: Wed, 01 Nov 2023 07:59:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece6288239743e91106675382cfcd819548aee82803abae921c4a440483ac2d3`  
		Last Modified: Wed, 01 Nov 2023 08:01:29 GMT  
		Size: 26.0 MB (25992576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d3edea3b8df240ef6a3d14aebdce6f270612a5067a478a91ae3701683adcd`  
		Last Modified: Wed, 01 Nov 2023 08:01:25 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:d0b8fb6c3786ee9e3912b10efd165aa5324820d8b411230aefbab0cf0c0639d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59392519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51b56c8ba9bce4bb37ad88b4c7a780136844f9462b496b333a6c55769c02a80`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:39 GMT
ADD file:f016ddd8ef89ed2b1825b3df9abc595f7e774f9a607e3481272e622153b57aaf in / 
# Wed, 01 Nov 2023 00:39:40 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 10:16:57 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 01 Nov 2023 10:16:57 GMT
WORKDIR /usr/src/perl
# Wed, 01 Nov 2023 10:58:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 01 Nov 2023 10:58:57 GMT
WORKDIR /usr/src/app
# Wed, 01 Nov 2023 10:58:58 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:36a7e611445c645573e630ead3c9d0a62139e195288b4e02b8a4dba6e0118b73`  
		Last Modified: Wed, 01 Nov 2023 00:45:00 GMT  
		Size: 27.8 MB (27846916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1121b77daf371f310a5fa441b89a136021e5ef7090bc64c164bfd4fbcd08d1dd`  
		Last Modified: Wed, 01 Nov 2023 13:26:35 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147e4392a6d1866bad233fbeaf96934ed0a449ccb063ccb82feef9ac9ecf2b8b`  
		Last Modified: Wed, 01 Nov 2023 13:28:09 GMT  
		Size: 31.5 MB (31545269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6c9430e0afd68aa4fadbf0e1a00f482e4c29bea6671e7cdf75226b0d972455`  
		Last Modified: Wed, 01 Nov 2023 13:28:01 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
