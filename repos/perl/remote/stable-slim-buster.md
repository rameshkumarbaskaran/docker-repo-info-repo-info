## `perl:stable-slim-buster`

```console
$ docker pull perl@sha256:94f1cf65e9c3382d4f6a0a33fd57bf2b65a82de6b5a1395c7dd40704bc060d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:stable-slim-buster` - linux; amd64

```console
$ docker pull perl@sha256:810506e73cad559648792c1cef750ea9208d9c567571db6402599938927878da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54510788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec62a59e11114bcd81e0ce50e5c76f9074e3e3fba620146c1498132cbdb12c6`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:29 GMT
ADD file:20e7ad6bec617357895302b08431eb3430cce3113bdf0a8ff9827115f858d313 in / 
# Thu, 27 Jul 2023 23:25:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 07:12:04 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 07:12:04 GMT
WORKDIR /usr/src/perl
# Fri, 28 Jul 2023 07:17:27 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Fri, 28 Jul 2023 07:17:28 GMT
WORKDIR /
# Fri, 28 Jul 2023 07:17:28 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:3240fe174df9a5a4923c4b52f1d887dd1ad1a9ee69245c1fb867f399167584dd`  
		Last Modified: Thu, 27 Jul 2023 23:30:49 GMT  
		Size: 27.2 MB (27187431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d47a5afeba760b590c5a05b01fe46b42336275eb6d5c63556e8bf808838ddc5`  
		Last Modified: Fri, 28 Jul 2023 10:36:12 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202ef04a9de9d76a854f864aa54fcbb14eab829ec7e865bb6cae280837e086e7`  
		Last Modified: Fri, 28 Jul 2023 10:36:17 GMT  
		Size: 27.3 MB (27323189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:stable-slim-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:8bae10da5cca44433f3ccbb311528671f50576ad9cdc26b7859a59d611ca330c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46695211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33806d3ba1b78e78c420fd4ed6a56b1ee8c86eb97c1e07fdf81f0319436fc6d`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:58:45 GMT
ADD file:3b46f6e6d897230250406ffac4282fec14a69ec0f54406c32cb9b0a4cfbabd3a in / 
# Thu, 27 Jul 2023 23:58:46 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 07:35:00 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 07:35:00 GMT
WORKDIR /usr/src/perl
# Fri, 28 Jul 2023 07:40:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Fri, 28 Jul 2023 07:40:36 GMT
WORKDIR /
# Fri, 28 Jul 2023 07:40:36 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:e744294d4f6feeafa673e883001a4539ae77771e6b7a913c7f0bdd38a447de77`  
		Last Modified: Fri, 28 Jul 2023 00:04:38 GMT  
		Size: 22.8 MB (22795588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e687a05d40fc28f908e824352dca4de4a7e05d4a3b55bfa8df0da61c92516bb`  
		Last Modified: Fri, 28 Jul 2023 11:10:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe56982085ab6107ece71a40b2900661624523fff1ae1abaeefb9be039aa8e91`  
		Last Modified: Fri, 28 Jul 2023 11:10:34 GMT  
		Size: 23.9 MB (23899453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:stable-slim-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:8779a1bb0075589f03c1dcc499b32d49d46d6aea6090a6cc07505b91a46ed66a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51927766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac0bbabb05d80740dcce35806318c874b864981d027561e5b68cc6a45fd378f`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:29 GMT
ADD file:ff126e7e4d046d566ea77f196c35d57f2d755b935cda365c5e3bba5f4d18ebf2 in / 
# Thu, 27 Jul 2023 23:43:29 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 07:05:27 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 07:05:27 GMT
WORKDIR /usr/src/perl
# Fri, 28 Jul 2023 07:09:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Fri, 28 Jul 2023 07:09:57 GMT
WORKDIR /
# Fri, 28 Jul 2023 07:09:57 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:d71ee974c4e69baa159b185ea2bebfc5b3d814a08167ed09a79596f4707642c0`  
		Last Modified: Thu, 27 Jul 2023 23:47:51 GMT  
		Size: 26.0 MB (25967808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6783fff81533b90d3c3d717f21735ade07d882028513f010a6cecf267849e6e4`  
		Last Modified: Fri, 28 Jul 2023 09:54:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04afbf5b14df554582dbaec8f5c1412cf93bbdd51e144c5745adad6fb11c1342`  
		Last Modified: Fri, 28 Jul 2023 09:54:13 GMT  
		Size: 26.0 MB (25959789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:stable-slim-buster` - linux; 386

```console
$ docker pull perl@sha256:975bb6e8bc00f9d09c68ff4139f28597052394560c991bd4afab16433b8d43d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59296912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83213e377c9393d740617ba66e1f1b0a838cc7c12257c81e3bf1aaad0f49de6`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:38 GMT
ADD file:a97f1ea317cafcf2810dfbe8ff5dfde5c43414d9cd1480b4e5f49d3ada8633f7 in / 
# Thu, 27 Jul 2023 23:39:38 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:48:22 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 28 Jul 2023 00:48:22 GMT
WORKDIR /usr/src/perl
# Fri, 28 Jul 2023 00:57:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Fri, 28 Jul 2023 00:57:46 GMT
WORKDIR /
# Fri, 28 Jul 2023 00:57:46 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:7eefe1e1e0f6af56fb4d37f33d6efcd121b57a2c33f6ce8272858d586e51f9d0`  
		Last Modified: Thu, 27 Jul 2023 23:44:57 GMT  
		Size: 27.8 MB (27846808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187ff58b5d6922d30276d47511ff6a13ca84edbb02617ed2c6413a476ea43b94`  
		Last Modified: Fri, 28 Jul 2023 03:49:35 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a482291b2e8cc78b73257cecd4f6d854cd38d40601d43a541ee9fd19388213`  
		Last Modified: Fri, 28 Jul 2023 03:49:42 GMT  
		Size: 31.4 MB (31449937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
