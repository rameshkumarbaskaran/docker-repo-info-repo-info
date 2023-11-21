## `perl:5-slim-threaded-buster`

```console
$ docker pull perl@sha256:df7a84bd1350cee92f264b1d9f0f06620c1182c7deba5bcde9f2560d83044572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:5-slim-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:84e1be878ec05852fdee950ea1783a6fdc5a5cbd873d4accb3d00c20c9b65667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54573415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2d79790d31b1eb553dd37ac0199bbea712089e811617bf804feade8e2cbdd6`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:26:09 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 21 Nov 2023 06:26:09 GMT
WORKDIR /usr/src/perl
# Tue, 21 Nov 2023 06:50:27 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Tue, 21 Nov 2023 06:50:28 GMT
WORKDIR /usr/src/app
# Tue, 21 Nov 2023 06:50:28 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c9e6a0beb8102e6e4484da6fa9a020eabbf35207c975f5616538a4ac2801e0`  
		Last Modified: Tue, 21 Nov 2023 08:39:06 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a312038c05ab15c641a8ec3b019f49b824fb82fd12161aefa32583c14b368610`  
		Last Modified: Tue, 21 Nov 2023 08:40:24 GMT  
		Size: 27.4 MB (27385626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a02870e4aa2fdc15aca58ac703ec5f72a8da0f7b61862b16fbf4887ca13907c`  
		Last Modified: Tue, 21 Nov 2023 08:40:19 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:6713107bd7ed54361c2d675d2020d9da02652e92d1474c5d0c13b95841ea79d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46719189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802da971835c0d677bf9c8838ec9e7dc3e13143c301289ae9544a8aab6f41bd3`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:22 GMT
ADD file:407ef80699946b8a8560ae436dfc9ca6148067b3012c02b4cb4e54d6d0aca674 in / 
# Tue, 21 Nov 2023 03:58:22 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:29:54 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 21 Nov 2023 04:29:54 GMT
WORKDIR /usr/src/perl
# Tue, 21 Nov 2023 04:53:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Tue, 21 Nov 2023 04:53:21 GMT
WORKDIR /usr/src/app
# Tue, 21 Nov 2023 04:53:21 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:d0b016a8027330736e9ca5c23b846a6a9c1eb0a32da6459047c95d22e9544cb7`  
		Last Modified: Tue, 21 Nov 2023 04:03:19 GMT  
		Size: 22.8 MB (22795884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2377a08a131e111c9f41f7522692d2d8f4e545680a1ae58f37f4195d9cc4ec5d`  
		Last Modified: Tue, 21 Nov 2023 06:42:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e6c7150ce5173f1ffa0d83c3569cadeb642debcb643fd87f314daa2057a520`  
		Last Modified: Tue, 21 Nov 2023 06:44:23 GMT  
		Size: 23.9 MB (23922971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c786d389d13aa00cc0945ec95fc8eac2dbe74ae028949026e906ca890f50240`  
		Last Modified: Tue, 21 Nov 2023 06:44:15 GMT  
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
$ docker pull perl@sha256:6dc34fd28d1ae57ade755dae5cb451761ff84ee14c20bb55257e8c8d9e9419e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59392634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51da1d4dc8b4434b597196c03c09fc8f92edf1658a6d3fc068f8493053d4e14d`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Tue, 21 Nov 2023 04:40:37 GMT
ADD file:a04f70df2aa61b210935e80ad2a655ad282407ef0b8e8e0acf47479c73f64f95 in / 
# Tue, 21 Nov 2023 04:40:38 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:11:52 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 21 Nov 2023 05:11:52 GMT
WORKDIR /usr/src/perl
# Tue, 21 Nov 2023 05:55:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Tue, 21 Nov 2023 05:55:19 GMT
WORKDIR /usr/src/app
# Tue, 21 Nov 2023 05:55:19 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:071d917b80792914c4da1ecc1adf7e2503440a8c7a2a5508542e0850d9187060`  
		Last Modified: Tue, 21 Nov 2023 04:46:12 GMT  
		Size: 27.8 MB (27846916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec5851faef42ba0487a82ae13df788da379aa99dc37d77640f32f0f4b91caf9`  
		Last Modified: Tue, 21 Nov 2023 09:10:06 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d77b6e149226c9d941546364dce2db6fa6074ea64f8d46302756e9f6b22113a`  
		Last Modified: Tue, 21 Nov 2023 09:11:32 GMT  
		Size: 31.5 MB (31545386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5cbb58d463449ae5fffcaca23a59da7ef7058be3964f727d913197c1edb41a`  
		Last Modified: Tue, 21 Nov 2023 09:11:24 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
