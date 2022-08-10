## `varnish:old`

```console
$ docker pull varnish@sha256:9bc3c81f65e54fe2a20032bc9da4a4ef2122036801d45dcff396f9e48a042ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:91c40dbb4ffb0eac8b3ccfdef33b66c8a7e1cb79a35b6d9370437c75f7ccd58c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101190284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caf0f67260e44f908f4535ee6794f693861988d6c1bda2311945fb82083288d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:39:11 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Aug 2022 15:41:25 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Aug 2022 15:41:25 GMT
WORKDIR /etc/varnish
# Tue, 02 Aug 2022 15:41:25 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 02 Aug 2022 15:41:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Aug 2022 15:41:26 GMT
EXPOSE 80 8443
# Tue, 02 Aug 2022 15:41:26 GMT
CMD []
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7fe56cfe58c70a0971620f9dbc39382b0e3bf53f8fcbea4ad6953cafc46b0b`  
		Last Modified: Tue, 02 Aug 2022 15:44:54 GMT  
		Size: 69.8 MB (69823054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34916b3133765331edc9e9bb054df3841cc2bda1acf24bd167a5f525073dc87`  
		Last Modified: Tue, 02 Aug 2022 15:44:44 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7c3d802dc2e7fe766778ba54e48633421dc875a087efceea831a254ca4925622
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77807084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6585bbb533608729231065c84e1179362a919001751ec67b363f511c94016674`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 12 Jul 2022 00:59:54 GMT
ADD file:ae890621b36ff6e27364bb7316b5bd4319a820ddf7e65565c6201eb11d70fde9 in / 
# Tue, 12 Jul 2022 00:59:55 GMT
CMD ["bash"]
# Wed, 13 Jul 2022 07:01:15 GMT
ENV VARNISH_SIZE=100M
# Wed, 13 Jul 2022 07:06:57 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 13 Jul 2022 07:06:58 GMT
WORKDIR /etc/varnish
# Wed, 13 Jul 2022 07:06:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 13 Jul 2022 07:06:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 13 Jul 2022 07:06:59 GMT
EXPOSE 80 8443
# Wed, 13 Jul 2022 07:07:00 GMT
CMD []
```

-	Layers:
	-	`sha256:314cda9d0ef2282082d2bd0efd7659e0d9edb3ceae8e7919d990bcf95cbb3d2b`  
		Last Modified: Tue, 12 Jul 2022 01:12:37 GMT  
		Size: 26.6 MB (26560559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe4c1024f00f2d9e87fb8571a9a87263d63c9cdd8b3b504e1fb44cbe5beb732`  
		Last Modified: Wed, 13 Jul 2022 07:16:17 GMT  
		Size: 51.2 MB (51246051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5549d87b127deeb9dea5cfad2a1912bcabbb94e6827be9f2e0ce7573cd768889`  
		Last Modified: Wed, 13 Jul 2022 07:15:49 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b97b0600db79c50598df5f04358b4e371bc2974edfb18bfebca0a810b03c02d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95301977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffec39973e1d7b23274e0ee5673efceee17eafa2a5b0b2648b8f7df742b9d108`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:26:20 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Aug 2022 17:28:27 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 02 Aug 2022 17:28:27 GMT
WORKDIR /etc/varnish
# Tue, 02 Aug 2022 17:28:29 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 02 Aug 2022 17:28:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Aug 2022 17:28:30 GMT
EXPOSE 80 8443
# Tue, 02 Aug 2022 17:28:31 GMT
CMD []
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db09e29bd8b78f01cc399fa0381a019e666e65ab3f6290e17d488ee4f52b2bf8`  
		Last Modified: Tue, 02 Aug 2022 17:31:55 GMT  
		Size: 65.2 MB (65247199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f2b3237ba8b7fd5318e765dfb1cdeea50a6acd1756528d7832e6178e56bdfd`  
		Last Modified: Tue, 02 Aug 2022 17:31:46 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:ccd17e9d90f3b2f114cb8c74aea52f0e73e779bc76c2c2a8ff721d407b08f716
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102674813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e167342d8f210738bcfbf355588b1f4e0af8fcf06c69a9700f853dc17ca994`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:50:05 GMT
ENV VARNISH_SIZE=100M
# Wed, 10 Aug 2022 00:07:44 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 10 Aug 2022 00:07:44 GMT
WORKDIR /etc/varnish
# Wed, 10 Aug 2022 00:07:46 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 10 Aug 2022 00:07:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 10 Aug 2022 00:07:47 GMT
EXPOSE 80 8443
# Wed, 10 Aug 2022 00:07:48 GMT
CMD []
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e835b4c612574327b5b84be4336d5c4cefc6d962aa891f293485045816234555`  
		Last Modified: Wed, 10 Aug 2022 00:12:31 GMT  
		Size: 70.3 MB (70300285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55daeb5d6b040fe6d23cee0ce4c9003173bb9a45baa7fe60960b9598c8a04e48`  
		Last Modified: Wed, 10 Aug 2022 00:12:22 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:d13325ee512667be29ade02c614b9e03695b551d7ac237b03e104f8900b21656
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100361746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310d4e7eb6423290cbbb21aa9f6aa398601737a7037b2018dfc27ef63fb5e61c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 01:39:47 GMT
ENV VARNISH_SIZE=100M
# Wed, 03 Aug 2022 01:44:30 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 03 Aug 2022 01:44:33 GMT
WORKDIR /etc/varnish
# Wed, 03 Aug 2022 01:44:33 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 03 Aug 2022 01:44:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 03 Aug 2022 01:44:34 GMT
EXPOSE 80 8443
# Wed, 03 Aug 2022 01:44:34 GMT
CMD []
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec340682e7f19ec10576a783f90c37d5ecbb077591ec21290529a24587ea91a`  
		Last Modified: Wed, 03 Aug 2022 01:53:19 GMT  
		Size: 65.1 MB (65088500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c345ba7f9213a7bca949a637135d8caf2d8cd4a09b5a2111ed2b47e78930d2`  
		Last Modified: Wed, 03 Aug 2022 01:53:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:4b16cb3b466bbe809c4833e2631cd4a9ddf572227e11c2fb3ce158a52465a752
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81623472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426be98166563a81501f737bf7edd9103507a566117a5395e75a6d54d80ada03`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 12 Jul 2022 00:43:45 GMT
ADD file:70135711d42f7b2b32586e31afb57a0590019326efa82abf1402dc7a8f02a3f2 in / 
# Tue, 12 Jul 2022 00:43:49 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 19:13:57 GMT
ENV VARNISH_SIZE=100M
# Tue, 12 Jul 2022 19:19:47 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.0.2.tgz -o $tmpdir/orig.tgz;     echo "5eb08345c95152639266b7ad241185188477f8fd04e88e4dfda1579719a1a413790a0616f25d70994f6d3b8f7640ea80926ece7c547555dad856fd9f6960c9a3  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.2|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 12 Jul 2022 19:19:57 GMT
WORKDIR /etc/varnish
# Tue, 12 Jul 2022 19:19:57 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 12 Jul 2022 19:19:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 12 Jul 2022 19:19:59 GMT
EXPOSE 80 8443
# Tue, 12 Jul 2022 19:20:00 GMT
CMD []
```

-	Layers:
	-	`sha256:447abc12b0c6da6e339b4fa17a2a7dd672d6f0631d30ee44c28b8b06e78884bd`  
		Last Modified: Tue, 12 Jul 2022 00:53:41 GMT  
		Size: 29.6 MB (29640209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f44713e40e8cd034f4c8f4dd815e5302835db628ffb0d6f606de6a30b3e909c`  
		Last Modified: Tue, 12 Jul 2022 19:28:33 GMT  
		Size: 52.0 MB (51982789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a43b712b028475ec29bca3a805cc61d86ec779b321fcd68dcdf093c4f9cfc1e`  
		Last Modified: Tue, 12 Jul 2022 19:28:25 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
