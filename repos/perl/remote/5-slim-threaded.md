## `perl:5-slim-threaded`

```console
$ docker pull perl@sha256:896da795330509080f12a9d61660a9b8d0c77bb2f13186f3c661e5cd0c9f64b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:5-slim-threaded` - linux; amd64

```console
$ docker pull perl@sha256:c2efd77c3f585b6059b71919b398271497185733a00b0838a1484f815057b185
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57659524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26a5d0875356f29aab8ebf8ec80265f396165c70d0399520877f506622d6f14`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:44 GMT
ADD file:209589a8bdb5a3788ee42ecdbccbbb561835dab96b0d8286bb5a2229d2f41be7 in / 
# Thu, 27 Jul 2023 23:24:45 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 07:00:46 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 07:00:46 GMT
WORKDIR /usr/src/perl
# Fri, 28 Jul 2023 07:41:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Fri, 28 Jul 2023 07:41:51 GMT
WORKDIR /
# Fri, 28 Jul 2023 07:41:51 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:648e0aadf75ac2ef63c5390adc6dc14fde37a5ad88c2870ea604df0a9c0eb4e5`  
		Last Modified: Thu, 27 Jul 2023 23:29:26 GMT  
		Size: 29.1 MB (29124532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749bf2df4351013b33de440f507cef216706d04769a6d25c1e5f4b8660fc1ce7`  
		Last Modified: Fri, 28 Jul 2023 10:35:25 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f895f269ecb1717aff8d51b08347cb6b258c6cb813d2ba36901d50a66b326806`  
		Last Modified: Fri, 28 Jul 2023 10:37:36 GMT  
		Size: 28.5 MB (28534824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:e6491573f881fbdbd35c87580a83776406b2bec5e400f9ccb0d8de26e245bcef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49637045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c9519af2591311a7123db794379f74f80d683899136177024f83644b7cf58`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:57:46 GMT
ADD file:b23161e9856801127e0136a920bcf075410ac23de605c82ca91d285b9f35941c in / 
# Thu, 27 Jul 2023 23:57:47 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 07:23:29 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 07:23:29 GMT
WORKDIR /usr/src/perl
# Fri, 28 Jul 2023 08:04:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Fri, 28 Jul 2023 08:04:58 GMT
WORKDIR /
# Fri, 28 Jul 2023 08:04:58 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:bb5b735234291ca6f672f489206ea5b6354d358f7d75a05036bdf84a6858d9f9`  
		Last Modified: Fri, 28 Jul 2023 00:03:11 GMT  
		Size: 24.8 MB (24805329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1036ed078d80aa9ae4b75b9ab6bcddd2df9c010b8b6748e2788f3ce0a2785258`  
		Last Modified: Fri, 28 Jul 2023 11:09:40 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0689ef1bcf0e9e502c888121d673151e1fa9187186c617ca726f04c447936f7b`  
		Last Modified: Fri, 28 Jul 2023 11:11:57 GMT  
		Size: 24.8 MB (24831549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c1fade7a615f8d5e429d8108c6e2637f92b6fd38d00ff7cd8bc9d5b543d39c5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56476060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4522432a753286798e52c9ac45fa32caaeac038f5632df2edb780151e4b29851`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:00 GMT
ADD file:1de2ba0dc88aa343332814e19adc6b850d08e62c31589fe902b8eb2cb465934e in / 
# Thu, 27 Jul 2023 23:43:00 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 06:55:56 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 06:55:56 GMT
WORKDIR /usr/src/perl
# Fri, 28 Jul 2023 07:29:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Fri, 28 Jul 2023 07:29:48 GMT
WORKDIR /
# Fri, 28 Jul 2023 07:29:48 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:90524f7dc01b4ce9b387992acc6cbdbcc2a9ee8c6addfd632429ca06ea18751e`  
		Last Modified: Thu, 27 Jul 2023 23:46:17 GMT  
		Size: 29.2 MB (29157226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8e9233af32930a70dcd925cd18ead0111e95bf5f5d45ebf2c5d9cf7ed4a6eb`  
		Last Modified: Fri, 28 Jul 2023 09:53:25 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ee6d4cda5058c3404875e462f39b72e334aae926fdbf88fc981824253a5bb`  
		Last Modified: Fri, 28 Jul 2023 09:55:32 GMT  
		Size: 27.3 MB (27318666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-threaded` - linux; 386

```console
$ docker pull perl@sha256:dc8f434fa912755c01ac8ab736844681f264384b2764466b8a720af114a9d777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57725687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603c4c453a4e171d60fa085e5f381709f72068599f46d9a64c6ee5ad03786a27`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:56 GMT
ADD file:3d6e6f3e900e480a7e060fcaf57313c0f954bf906967a7fa0317567c387cf5aa in / 
# Thu, 27 Jul 2023 23:38:57 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:29:06 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 00:29:06 GMT
WORKDIR /usr/src/perl
# Fri, 28 Jul 2023 01:08:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Fri, 28 Jul 2023 01:08:44 GMT
WORKDIR /
# Fri, 28 Jul 2023 01:08:44 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:3a8b0c4b1a83609d978d576be6174f951ff27084d7c9aef91892b60b223a5104`  
		Last Modified: Thu, 27 Jul 2023 23:43:26 GMT  
		Size: 30.1 MB (30141788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3d7be80320fa7cd198643a136d11d49aed0a6a65c6ed6d27fe3a8761104577`  
		Last Modified: Fri, 28 Jul 2023 03:48:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c45343d7527c3249b58da6aaa631942b536a39f02a0e84d2d18025e7ede165`  
		Last Modified: Fri, 28 Jul 2023 03:50:13 GMT  
		Size: 27.6 MB (27583731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
