## `perl:devel-slim-threaded-buster`

```console
$ docker pull perl@sha256:bb058a4fa9401a5f7d217036655d375225311b3bb01d7f34b0d1f82faf7ff978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:devel-slim-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:b5877be3c54c420f9365d20dc8d066d763bcd8a51fd5099d25b84942f964a332
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54455311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ae878daef917757805833b9533e977264df0a8063326ae49c12faf7416ea30`
-	Default Command: `["perl5.37.8","-de0"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 10:55:35 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 24 Jan 2023 19:14:00 GMT
WORKDIR /usr/src/perl
# Tue, 24 Jan 2023 22:00:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.8.tar.xz -o perl-5.37.8.tar.xz     && echo 'eca6396a4b1aa7a38ef467ce54ed897cc84ba948fad0f90aeb210e57b04daf3c *perl-5.37.8.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.8.tar.xz -C /usr/src/perl     && rm perl-5.37.8.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Tue, 24 Jan 2023 22:00:28 GMT
WORKDIR /
# Tue, 24 Jan 2023 22:00:29 GMT
CMD ["perl5.37.8" "-de0"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dc22116046662510041d255ef9de3306e407da2882fd611910bba3fe3683be`  
		Last Modified: Tue, 24 Jan 2023 22:04:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5507ea9ac0110598a925ab9edb8ead99c33c4cfc1e5ca316a8d0de724a7771`  
		Last Modified: Tue, 24 Jan 2023 22:11:59 GMT  
		Size: 27.3 MB (27314790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-slim-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:36887b4ce671db6e507e61fa53dc513a716b923d4515914005aba9c18afff5d6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46606996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf55c4b7fa9f0710974a97508c6d3d654687e81323fb6d1abb2fbe232f619ce7`
-	Default Command: `["perl5.37.8","-de0"]`

```dockerfile
# Wed, 11 Jan 2023 04:01:11 GMT
ADD file:360ea34974de7bba698a1a4e78149a2da671264dbf02678aef09bcd3f592c229 in / 
# Wed, 11 Jan 2023 04:01:12 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 08:13:35 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 24 Jan 2023 18:56:13 GMT
WORKDIR /usr/src/perl
# Tue, 24 Jan 2023 21:51:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.8.tar.xz -o perl-5.37.8.tar.xz     && echo 'eca6396a4b1aa7a38ef467ce54ed897cc84ba948fad0f90aeb210e57b04daf3c *perl-5.37.8.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.8.tar.xz -C /usr/src/perl     && rm perl-5.37.8.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Tue, 24 Jan 2023 21:51:33 GMT
WORKDIR /
# Tue, 24 Jan 2023 21:51:33 GMT
CMD ["perl5.37.8" "-de0"]
```

-	Layers:
	-	`sha256:75680cfdd833613d913b856d8c584fa88c596b93732050a582a5fe937df3a9e6`  
		Last Modified: Wed, 11 Jan 2023 04:08:41 GMT  
		Size: 22.7 MB (22748873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2310adac7d82c782ae4d7ec47d82d177069d34eb42a5126bd69e9b4d319be3`  
		Last Modified: Tue, 24 Jan 2023 21:59:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabc25c62681fe4eb043c719ae227a54f6d17da534eadb2d066db38c0caa6eb0`  
		Last Modified: Tue, 24 Jan 2023 22:10:14 GMT  
		Size: 23.9 MB (23857987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-slim-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:a896a924766443efe706f84135f895f636f4809dfa518428506a36ef84a8dfa9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51848560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a41906a7f65f5cac3d076faef7303127d9e5242d2eab35e33123e4c52c6cbbe`
-	Default Command: `["perl5.37.8","-de0"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:54 GMT
ADD file:cf6ecb1d6b034b0d4fc309542cb25fff0c997661b323f524ecc258ac323e43f6 in / 
# Sat, 04 Feb 2023 06:17:55 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:40:58 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Sat, 04 Feb 2023 09:40:58 GMT
WORKDIR /usr/src/perl
# Sat, 04 Feb 2023 11:54:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.8.tar.xz -o perl-5.37.8.tar.xz     && echo 'eca6396a4b1aa7a38ef467ce54ed897cc84ba948fad0f90aeb210e57b04daf3c *perl-5.37.8.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.8.tar.xz -C /usr/src/perl     && rm perl-5.37.8.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Sat, 04 Feb 2023 11:54:35 GMT
WORKDIR /
# Sat, 04 Feb 2023 11:54:35 GMT
CMD ["perl5.37.8" "-de0"]
```

-	Layers:
	-	`sha256:bd2853c1424a5596deda2f31e1f82920613a03c667c3ff58cb461340b7bb89cd`  
		Last Modified: Sat, 04 Feb 2023 06:22:04 GMT  
		Size: 25.9 MB (25922631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77faefe9515c2ef2858f44a113906d7e7556f5166a7424d37d0cb123b7181c1d`  
		Last Modified: Sat, 04 Feb 2023 11:58:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be985869ea877f47abdd8614b36208c1e18f3e9ecb025806948932804ff28008`  
		Last Modified: Sat, 04 Feb 2023 12:05:48 GMT  
		Size: 25.9 MB (25925760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-slim-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:861593eba0d43219b6ebd2e22a6054ef8f2c4e9fcf3110947e2b1c796cc624c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59272529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad166c010ef5534b42361431d39a26d7605f219c7ba3b2e69518796fb3cbde6`
-	Default Command: `["perl5.37.8","-de0"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:48 GMT
ADD file:060bbacc8df3d1b157ff409535b3ea29dd0b5667425e3dcf6e60556dcfa4e7f1 in / 
# Sat, 04 Feb 2023 07:49:48 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:52:57 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Sat, 04 Feb 2023 10:52:58 GMT
WORKDIR /usr/src/perl
# Sat, 04 Feb 2023 14:00:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.8.tar.xz -o perl-5.37.8.tar.xz     && echo 'eca6396a4b1aa7a38ef467ce54ed897cc84ba948fad0f90aeb210e57b04daf3c *perl-5.37.8.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.8.tar.xz -C /usr/src/perl     && rm perl-5.37.8.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Sat, 04 Feb 2023 14:00:20 GMT
WORKDIR /
# Sat, 04 Feb 2023 14:00:21 GMT
CMD ["perl5.37.8" "-de0"]
```

-	Layers:
	-	`sha256:8e0d975bedf8c90406704c677df48435cd2d53449ac9ab15a876323ceb95ff8f`  
		Last Modified: Sat, 04 Feb 2023 07:55:52 GMT  
		Size: 27.8 MB (27798503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5819b7078bf3f3be48a33ffd757690763dfdc8c7972bf0f372c1f47726fc0a0`  
		Last Modified: Sat, 04 Feb 2023 14:06:47 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f0430254a39689df1505f7d146109e172ea484c29c9ac25165408256c89580`  
		Last Modified: Sat, 04 Feb 2023 14:16:03 GMT  
		Size: 31.5 MB (31473891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
