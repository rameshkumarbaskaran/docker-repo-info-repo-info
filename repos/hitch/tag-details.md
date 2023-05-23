<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `hitch`

-	[`hitch:1`](#hitch1)
-	[`hitch:1.7`](#hitch17)
-	[`hitch:1.7.2`](#hitch172)
-	[`hitch:1.7.2-1`](#hitch172-1)
-	[`hitch:1.7.3`](#hitch173)
-	[`hitch:1.7.3-1`](#hitch173-1)
-	[`hitch:latest`](#hitchlatest)

## `hitch:1`

```console
$ docker pull hitch@sha256:d51d99b186aade9dd4830ffe2da37530750a2f75e07f0767f67f46ba1f5d3b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1` - linux; amd64

```console
$ docker pull hitch@sha256:ca330d657f8c093a47de0a3fa1fac6de63e910c0d4c0fb4e3b31a3bcee4a92bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33029490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565dce13d52a485bf741af18a4b7ba34bcb5116aa517f9979f6bd772d1a9e14d`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:42:42 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 20:42:42 GMT
ARG PKGVER=1
# Wed, 03 May 2023 20:42:42 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 20:42:42 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 20:42:42 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 20:45:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 20:45:00 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 20:45:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 20:45:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 20:45:00 GMT
EXPOSE 443
# Wed, 03 May 2023 20:45:00 GMT
CMD []
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5068fb84d96c68410d2be20fc4225f48dfa270dbc5b30b989f758f1ad5321d29`  
		Last Modified: Wed, 03 May 2023 20:47:06 GMT  
		Size: 1.6 MB (1625559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536fe63701960687ec7375f35e1c4a462045d6268be880184143f7a144bfb5f9`  
		Last Modified: Wed, 03 May 2023 20:47:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:bfe06ecd7baf8664063dafabfc67269e5c08fa2beee60045ca63da7d29cceb0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28109984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e80e6f4b4ac0406b6e6f3a596a00212adf2d771ea6830a6200e654270058a1`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:24:57 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 22:24:57 GMT
ARG PKGVER=1
# Wed, 03 May 2023 22:24:57 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 22:24:57 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 22:24:58 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 22:27:03 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 22:27:03 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 22:27:03 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 22:27:03 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 22:27:03 GMT
EXPOSE 443
# Wed, 03 May 2023 22:27:04 GMT
CMD []
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2dab1babd812b56d3e886093fe502a9104e86360c036925512f64fcf5f32e`  
		Last Modified: Wed, 03 May 2023 22:29:18 GMT  
		Size: 1.5 MB (1544920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09219df1ddb6a679b8ab5b0526ed93731bd464ef8bbb80ef08d367f2fe3ef70`  
		Last Modified: Wed, 03 May 2023 22:29:18 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:d1629f7d56021774230df5c34e353f7ac5e49b62644c4cc0066d318e4bd96c0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31659894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0fafc9d733edf9dba64b5b95814ca46540fbbb9f0dc3ef52d94315fd3e1bef`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:09:07 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 19:09:07 GMT
ARG PKGVER=1
# Wed, 03 May 2023 19:09:07 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 19:09:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 19:09:07 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 19:11:45 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 19:11:45 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 19:11:45 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 19:11:45 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 19:11:45 GMT
EXPOSE 443
# Wed, 03 May 2023 19:11:46 GMT
CMD []
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d452d8d83439efc46c6b37fed2cd2d54812801e1178d7c34fbb3080634fc529f`  
		Last Modified: Wed, 03 May 2023 19:13:44 GMT  
		Size: 1.6 MB (1606744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2260a81f4103e7411fa7d44f9e74200073c0bcd4c91c1bbc262db1218729be27`  
		Last Modified: Wed, 03 May 2023 19:13:44 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; 386

```console
$ docker pull hitch@sha256:8038ee914449710b1c88c0717c219a01a14290adeddf269e10ed92fcd84a9a79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34019411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f6718679c908b2e1555f63d337f2c20d2889a7c7a41f936566de2722f0b594`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:39:30 GMT
ADD file:8319fc1c1a3c0f2a6bb03636fe1fd0eb7fa52c58505d279e4366627452ea2104 in / 
# Tue, 23 May 2023 00:39:30 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:17:48 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 02:17:48 GMT
ARG PKGVER=1
# Tue, 23 May 2023 02:17:48 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 02:17:48 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 02:17:49 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 02:20:55 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 02:20:55 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 02:20:55 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 02:20:55 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 02:20:55 GMT
EXPOSE 443
# Tue, 23 May 2023 02:20:55 GMT
CMD []
```

-	Layers:
	-	`sha256:0f5d158483bd0ffef0c106b68514aece2ca0500d2990c830844277cbca7fe0bc`  
		Last Modified: Tue, 23 May 2023 00:44:28 GMT  
		Size: 32.4 MB (32388165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0552cf37dffe35777a972a2fbfdb0261a9dab866e16b0cbc255be1ea4ac1ce93`  
		Last Modified: Tue, 23 May 2023 02:23:26 GMT  
		Size: 1.6 MB (1630829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab59e29f2218e25e27a6bfe94a5e89f0a3072361f36219c75fb7ab081c755ed`  
		Last Modified: Tue, 23 May 2023 02:23:26 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; ppc64le

```console
$ docker pull hitch@sha256:e9b5286e8e0bc3ccfc33c9349e6b63a803321e5363dd87a10448da6c48f5ef9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36967394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef237ebe0340d5c57ca79403a2a8fb0185b42d9f8b985263ad6c1466989494d4`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 01:17:35 GMT
ADD file:719aea085739ec41c255f35070ca652d4e356c5ee62c8237f8ebc7389feb8e38 in / 
# Tue, 23 May 2023 01:17:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:56:44 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 03:56:44 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:56:45 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:56:45 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:56:48 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 04:01:36 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 04:01:36 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 04:01:36 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 04:01:37 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 04:01:37 GMT
EXPOSE 443
# Tue, 23 May 2023 04:01:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b6c83d2f160e7e38990586d26caa105ff577368a887fd754ae4634cdbfec83ff`  
		Last Modified: Tue, 23 May 2023 01:22:03 GMT  
		Size: 35.3 MB (35280911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025635a981d45424d281e8d94eb0ddf5ebf5079200c85ba9948aea42baa0c32b`  
		Last Modified: Tue, 23 May 2023 04:06:26 GMT  
		Size: 1.7 MB (1686066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1445e943c8f14237987563f07add91ea058e5529a487ecf009b2b08e6a756e`  
		Last Modified: Tue, 23 May 2023 04:06:25 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; s390x

```console
$ docker pull hitch@sha256:12e21419e43bbf8ff6e18c60fadc7404b20bd3e3f026df5ff56059c9e1f7175c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31264475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dee568490617674e36ccb727444753eae5a02daeb977d2bebe375f21acfba27`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:42:52 GMT
ADD file:23b1e12559302529556a94a1d4098dbdb454e263265258b940c2b2d23a97c121 in / 
# Tue, 23 May 2023 00:42:54 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:27:20 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 03:27:20 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:27:20 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:27:20 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:27:20 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 03:28:40 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 03:28:40 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 03:28:40 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 03:28:40 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 03:28:40 GMT
EXPOSE 443
# Tue, 23 May 2023 03:28:40 GMT
CMD []
```

-	Layers:
	-	`sha256:9c24ec455bdb6a9ad0d033c7cce8e71dd5bdbbe53a86d5feeb8d4cb7804fb8e5`  
		Last Modified: Tue, 23 May 2023 00:45:47 GMT  
		Size: 29.6 MB (29642170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfffa71d72401278590e0bd1d1629aabea25dc2c971d63c00a8acace2d1877a0`  
		Last Modified: Tue, 23 May 2023 03:30:33 GMT  
		Size: 1.6 MB (1621889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb2959ffed3113cab3c7f0e0e8144cde4bbb0efbf393fc7a5b7d4908dcaf07`  
		Last Modified: Tue, 23 May 2023 03:30:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7`

```console
$ docker pull hitch@sha256:d51d99b186aade9dd4830ffe2da37530750a2f75e07f0767f67f46ba1f5d3b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.7` - linux; amd64

```console
$ docker pull hitch@sha256:ca330d657f8c093a47de0a3fa1fac6de63e910c0d4c0fb4e3b31a3bcee4a92bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33029490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565dce13d52a485bf741af18a4b7ba34bcb5116aa517f9979f6bd772d1a9e14d`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:42:42 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 20:42:42 GMT
ARG PKGVER=1
# Wed, 03 May 2023 20:42:42 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 20:42:42 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 20:42:42 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 20:45:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 20:45:00 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 20:45:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 20:45:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 20:45:00 GMT
EXPOSE 443
# Wed, 03 May 2023 20:45:00 GMT
CMD []
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5068fb84d96c68410d2be20fc4225f48dfa270dbc5b30b989f758f1ad5321d29`  
		Last Modified: Wed, 03 May 2023 20:47:06 GMT  
		Size: 1.6 MB (1625559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536fe63701960687ec7375f35e1c4a462045d6268be880184143f7a144bfb5f9`  
		Last Modified: Wed, 03 May 2023 20:47:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; arm variant v7

```console
$ docker pull hitch@sha256:bfe06ecd7baf8664063dafabfc67269e5c08fa2beee60045ca63da7d29cceb0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28109984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e80e6f4b4ac0406b6e6f3a596a00212adf2d771ea6830a6200e654270058a1`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:24:57 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 22:24:57 GMT
ARG PKGVER=1
# Wed, 03 May 2023 22:24:57 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 22:24:57 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 22:24:58 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 22:27:03 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 22:27:03 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 22:27:03 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 22:27:03 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 22:27:03 GMT
EXPOSE 443
# Wed, 03 May 2023 22:27:04 GMT
CMD []
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2dab1babd812b56d3e886093fe502a9104e86360c036925512f64fcf5f32e`  
		Last Modified: Wed, 03 May 2023 22:29:18 GMT  
		Size: 1.5 MB (1544920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09219df1ddb6a679b8ab5b0526ed93731bd464ef8bbb80ef08d367f2fe3ef70`  
		Last Modified: Wed, 03 May 2023 22:29:18 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:d1629f7d56021774230df5c34e353f7ac5e49b62644c4cc0066d318e4bd96c0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31659894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0fafc9d733edf9dba64b5b95814ca46540fbbb9f0dc3ef52d94315fd3e1bef`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:09:07 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 19:09:07 GMT
ARG PKGVER=1
# Wed, 03 May 2023 19:09:07 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 19:09:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 19:09:07 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 19:11:45 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 19:11:45 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 19:11:45 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 19:11:45 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 19:11:45 GMT
EXPOSE 443
# Wed, 03 May 2023 19:11:46 GMT
CMD []
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d452d8d83439efc46c6b37fed2cd2d54812801e1178d7c34fbb3080634fc529f`  
		Last Modified: Wed, 03 May 2023 19:13:44 GMT  
		Size: 1.6 MB (1606744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2260a81f4103e7411fa7d44f9e74200073c0bcd4c91c1bbc262db1218729be27`  
		Last Modified: Wed, 03 May 2023 19:13:44 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; 386

```console
$ docker pull hitch@sha256:8038ee914449710b1c88c0717c219a01a14290adeddf269e10ed92fcd84a9a79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34019411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f6718679c908b2e1555f63d337f2c20d2889a7c7a41f936566de2722f0b594`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:39:30 GMT
ADD file:8319fc1c1a3c0f2a6bb03636fe1fd0eb7fa52c58505d279e4366627452ea2104 in / 
# Tue, 23 May 2023 00:39:30 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:17:48 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 02:17:48 GMT
ARG PKGVER=1
# Tue, 23 May 2023 02:17:48 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 02:17:48 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 02:17:49 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 02:20:55 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 02:20:55 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 02:20:55 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 02:20:55 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 02:20:55 GMT
EXPOSE 443
# Tue, 23 May 2023 02:20:55 GMT
CMD []
```

-	Layers:
	-	`sha256:0f5d158483bd0ffef0c106b68514aece2ca0500d2990c830844277cbca7fe0bc`  
		Last Modified: Tue, 23 May 2023 00:44:28 GMT  
		Size: 32.4 MB (32388165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0552cf37dffe35777a972a2fbfdb0261a9dab866e16b0cbc255be1ea4ac1ce93`  
		Last Modified: Tue, 23 May 2023 02:23:26 GMT  
		Size: 1.6 MB (1630829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab59e29f2218e25e27a6bfe94a5e89f0a3072361f36219c75fb7ab081c755ed`  
		Last Modified: Tue, 23 May 2023 02:23:26 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; ppc64le

```console
$ docker pull hitch@sha256:e9b5286e8e0bc3ccfc33c9349e6b63a803321e5363dd87a10448da6c48f5ef9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36967394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef237ebe0340d5c57ca79403a2a8fb0185b42d9f8b985263ad6c1466989494d4`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 01:17:35 GMT
ADD file:719aea085739ec41c255f35070ca652d4e356c5ee62c8237f8ebc7389feb8e38 in / 
# Tue, 23 May 2023 01:17:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:56:44 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 03:56:44 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:56:45 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:56:45 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:56:48 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 04:01:36 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 04:01:36 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 04:01:36 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 04:01:37 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 04:01:37 GMT
EXPOSE 443
# Tue, 23 May 2023 04:01:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b6c83d2f160e7e38990586d26caa105ff577368a887fd754ae4634cdbfec83ff`  
		Last Modified: Tue, 23 May 2023 01:22:03 GMT  
		Size: 35.3 MB (35280911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025635a981d45424d281e8d94eb0ddf5ebf5079200c85ba9948aea42baa0c32b`  
		Last Modified: Tue, 23 May 2023 04:06:26 GMT  
		Size: 1.7 MB (1686066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1445e943c8f14237987563f07add91ea058e5529a487ecf009b2b08e6a756e`  
		Last Modified: Tue, 23 May 2023 04:06:25 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; s390x

```console
$ docker pull hitch@sha256:12e21419e43bbf8ff6e18c60fadc7404b20bd3e3f026df5ff56059c9e1f7175c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31264475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dee568490617674e36ccb727444753eae5a02daeb977d2bebe375f21acfba27`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:42:52 GMT
ADD file:23b1e12559302529556a94a1d4098dbdb454e263265258b940c2b2d23a97c121 in / 
# Tue, 23 May 2023 00:42:54 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:27:20 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 03:27:20 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:27:20 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:27:20 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:27:20 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 03:28:40 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 03:28:40 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 03:28:40 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 03:28:40 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 03:28:40 GMT
EXPOSE 443
# Tue, 23 May 2023 03:28:40 GMT
CMD []
```

-	Layers:
	-	`sha256:9c24ec455bdb6a9ad0d033c7cce8e71dd5bdbbe53a86d5feeb8d4cb7804fb8e5`  
		Last Modified: Tue, 23 May 2023 00:45:47 GMT  
		Size: 29.6 MB (29642170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfffa71d72401278590e0bd1d1629aabea25dc2c971d63c00a8acace2d1877a0`  
		Last Modified: Tue, 23 May 2023 03:30:33 GMT  
		Size: 1.6 MB (1621889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb2959ffed3113cab3c7f0e0e8144cde4bbb0efbf393fc7a5b7d4908dcaf07`  
		Last Modified: Tue, 23 May 2023 03:30:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.2`

```console
$ docker pull hitch@sha256:2d9cc2f00971e0bdf4a678cac70d6edd5b48c00993d245bd0db62a8b1d54111e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.7.2` - linux; amd64

```console
$ docker pull hitch@sha256:74019dbc698afbd5a10e2cb347aa8a572d2571ec2c6165d60200502949a2fbd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33028904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16c661aa6168abc4305003226ec94a5d122946ca62303526e0574a7a1606a6b`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:45:05 GMT
ARG SRCVER=1.7.2
# Wed, 03 May 2023 20:45:05 GMT
ARG PKGVER=1
# Wed, 03 May 2023 20:45:05 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 20:45:05 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 20:45:05 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Wed, 03 May 2023 20:46:43 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 20:46:43 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 20:46:43 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 20:46:44 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 20:46:44 GMT
EXPOSE 443
# Wed, 03 May 2023 20:46:44 GMT
CMD []
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e518832e83e5a7eb0bf2a0295b8c6d08b29bb23364493f95292cb13942e82b`  
		Last Modified: Wed, 03 May 2023 20:47:20 GMT  
		Size: 1.6 MB (1624971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75974984593c40e0f28f2e885deb4eb76eddb49913122f7c37420e3bcaa8ea3c`  
		Last Modified: Wed, 03 May 2023 20:47:20 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; arm variant v7

```console
$ docker pull hitch@sha256:c2fb9ade07f177bb3757f104a37a3891ae40d6b8e625e0308305b0192a82071a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28108959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcea46603bb63579228ea14fd78b7c36e1d758fb4af7bd5f324c01dc9ab07d6`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:27:20 GMT
ARG SRCVER=1.7.2
# Wed, 03 May 2023 22:27:20 GMT
ARG PKGVER=1
# Wed, 03 May 2023 22:27:20 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 22:27:20 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 22:27:20 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Wed, 03 May 2023 22:28:57 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 22:28:57 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 22:28:57 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 22:28:57 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 22:28:57 GMT
EXPOSE 443
# Wed, 03 May 2023 22:28:57 GMT
CMD []
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9160139e168af9811b76a6d895ef3c7440d6c4021c79ba0c45e2a7bd7b66f1`  
		Last Modified: Wed, 03 May 2023 22:29:31 GMT  
		Size: 1.5 MB (1543893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def112daed38d573dd3841a2d78ec6cbbf0e209af62a9643b19fad53ef6a7008`  
		Last Modified: Wed, 03 May 2023 22:29:31 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:c924b8d675d4742a98a9af86f7ff788c97b4458b2612659bdf920d9c4b4613e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31659098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d374936536837756830026217092e96ff59c5329b059c7b8db6b701aefc252c5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:11:59 GMT
ARG SRCVER=1.7.2
# Wed, 03 May 2023 19:11:59 GMT
ARG PKGVER=1
# Wed, 03 May 2023 19:11:59 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 19:12:00 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 19:12:00 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Wed, 03 May 2023 19:13:28 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 19:13:28 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 19:13:28 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 19:13:28 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 19:13:28 GMT
EXPOSE 443
# Wed, 03 May 2023 19:13:29 GMT
CMD []
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f09fd0d72136410c7ad5b51c26522f83cd759a0379e5816e924e2608485b8e`  
		Last Modified: Wed, 03 May 2023 19:13:57 GMT  
		Size: 1.6 MB (1605949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80168d86b1303babc0093dced4b43378e6fdf51f44c4dba97b4903955a4dd696`  
		Last Modified: Wed, 03 May 2023 19:13:57 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; 386

```console
$ docker pull hitch@sha256:1784bb3cc90a04b9f1d0d7b12716b0fac39220ff87baf5421fe0b162cbec05cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34018056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abff1422a0f763175c425a62e087f08e5e7fead9287ddbf945845e161b01f6c`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:39:30 GMT
ADD file:8319fc1c1a3c0f2a6bb03636fe1fd0eb7fa52c58505d279e4366627452ea2104 in / 
# Tue, 23 May 2023 00:39:30 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:21:11 GMT
ARG SRCVER=1.7.2
# Tue, 23 May 2023 02:21:11 GMT
ARG PKGVER=1
# Tue, 23 May 2023 02:21:11 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 02:21:11 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 02:21:11 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 23 May 2023 02:23:04 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 02:23:04 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 02:23:04 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 02:23:04 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 02:23:05 GMT
EXPOSE 443
# Tue, 23 May 2023 02:23:05 GMT
CMD []
```

-	Layers:
	-	`sha256:0f5d158483bd0ffef0c106b68514aece2ca0500d2990c830844277cbca7fe0bc`  
		Last Modified: Tue, 23 May 2023 00:44:28 GMT  
		Size: 32.4 MB (32388165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fa083c96300d2c89bd9171730144af8aca582a16d163c2cb8ed1cb29b385d3`  
		Last Modified: Tue, 23 May 2023 02:23:40 GMT  
		Size: 1.6 MB (1629475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf00415e113963832d912f35449fdae3f2c51b4cae619d784b85fe2801aa53a`  
		Last Modified: Tue, 23 May 2023 02:23:40 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; ppc64le

```console
$ docker pull hitch@sha256:6fa2699833f96d0bc0c1edb3aaff29fe319d3845b856020147cd4ca1d12b83b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36966506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767a07bd307569ab11622655b901ea76a114c019b3823388b4ee3a9a4b0db7ce`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 01:17:35 GMT
ADD file:719aea085739ec41c255f35070ca652d4e356c5ee62c8237f8ebc7389feb8e38 in / 
# Tue, 23 May 2023 01:17:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:01:53 GMT
ARG SRCVER=1.7.2
# Tue, 23 May 2023 04:01:54 GMT
ARG PKGVER=1
# Tue, 23 May 2023 04:01:54 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 04:01:54 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 04:01:54 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 23 May 2023 04:06:03 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 04:06:04 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 04:06:04 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 04:06:04 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 04:06:04 GMT
EXPOSE 443
# Tue, 23 May 2023 04:06:05 GMT
CMD []
```

-	Layers:
	-	`sha256:b6c83d2f160e7e38990586d26caa105ff577368a887fd754ae4634cdbfec83ff`  
		Last Modified: Tue, 23 May 2023 01:22:03 GMT  
		Size: 35.3 MB (35280911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaca712bf76fbe2f0a6242f971a33bdb3316269b568a83adbb9f257ed45fedc`  
		Last Modified: Tue, 23 May 2023 04:06:41 GMT  
		Size: 1.7 MB (1685177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba7766ef7f2592880167519133ffc0f376c44f67646d20140d73cc2e76f7d9d`  
		Last Modified: Tue, 23 May 2023 04:06:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; s390x

```console
$ docker pull hitch@sha256:63a4dd3d3a66996e3f653d23831157dc75695213bc33ce7c8e65951c5645ff2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31263978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d9a1a06b511b02a6231b2a11714620be250fcef957eedcc58f2be222f55754`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:42:52 GMT
ADD file:23b1e12559302529556a94a1d4098dbdb454e263265258b940c2b2d23a97c121 in / 
# Tue, 23 May 2023 00:42:54 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:28:52 GMT
ARG SRCVER=1.7.2
# Tue, 23 May 2023 03:28:52 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:28:52 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:28:52 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:28:53 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 23 May 2023 03:30:13 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 03:30:13 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 03:30:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 03:30:13 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 03:30:13 GMT
EXPOSE 443
# Tue, 23 May 2023 03:30:13 GMT
CMD []
```

-	Layers:
	-	`sha256:9c24ec455bdb6a9ad0d033c7cce8e71dd5bdbbe53a86d5feeb8d4cb7804fb8e5`  
		Last Modified: Tue, 23 May 2023 00:45:47 GMT  
		Size: 29.6 MB (29642170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7de11580e1879b459dbeefc114ada2b442f0f2a5ff5ee82fe86bb399fd572`  
		Last Modified: Tue, 23 May 2023 03:30:41 GMT  
		Size: 1.6 MB (1621391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd34c028b72ea8e1036059d23e0471f102c0868dc2c2eaee4af3a2bf430bffe`  
		Last Modified: Tue, 23 May 2023 03:30:41 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.2-1`

```console
$ docker pull hitch@sha256:2d9cc2f00971e0bdf4a678cac70d6edd5b48c00993d245bd0db62a8b1d54111e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.7.2-1` - linux; amd64

```console
$ docker pull hitch@sha256:74019dbc698afbd5a10e2cb347aa8a572d2571ec2c6165d60200502949a2fbd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33028904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16c661aa6168abc4305003226ec94a5d122946ca62303526e0574a7a1606a6b`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:45:05 GMT
ARG SRCVER=1.7.2
# Wed, 03 May 2023 20:45:05 GMT
ARG PKGVER=1
# Wed, 03 May 2023 20:45:05 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 20:45:05 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 20:45:05 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Wed, 03 May 2023 20:46:43 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 20:46:43 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 20:46:43 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 20:46:44 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 20:46:44 GMT
EXPOSE 443
# Wed, 03 May 2023 20:46:44 GMT
CMD []
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e518832e83e5a7eb0bf2a0295b8c6d08b29bb23364493f95292cb13942e82b`  
		Last Modified: Wed, 03 May 2023 20:47:20 GMT  
		Size: 1.6 MB (1624971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75974984593c40e0f28f2e885deb4eb76eddb49913122f7c37420e3bcaa8ea3c`  
		Last Modified: Wed, 03 May 2023 20:47:20 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:c2fb9ade07f177bb3757f104a37a3891ae40d6b8e625e0308305b0192a82071a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28108959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcea46603bb63579228ea14fd78b7c36e1d758fb4af7bd5f324c01dc9ab07d6`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:27:20 GMT
ARG SRCVER=1.7.2
# Wed, 03 May 2023 22:27:20 GMT
ARG PKGVER=1
# Wed, 03 May 2023 22:27:20 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 22:27:20 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 22:27:20 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Wed, 03 May 2023 22:28:57 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 22:28:57 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 22:28:57 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 22:28:57 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 22:28:57 GMT
EXPOSE 443
# Wed, 03 May 2023 22:28:57 GMT
CMD []
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9160139e168af9811b76a6d895ef3c7440d6c4021c79ba0c45e2a7bd7b66f1`  
		Last Modified: Wed, 03 May 2023 22:29:31 GMT  
		Size: 1.5 MB (1543893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def112daed38d573dd3841a2d78ec6cbbf0e209af62a9643b19fad53ef6a7008`  
		Last Modified: Wed, 03 May 2023 22:29:31 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:c924b8d675d4742a98a9af86f7ff788c97b4458b2612659bdf920d9c4b4613e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31659098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d374936536837756830026217092e96ff59c5329b059c7b8db6b701aefc252c5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:11:59 GMT
ARG SRCVER=1.7.2
# Wed, 03 May 2023 19:11:59 GMT
ARG PKGVER=1
# Wed, 03 May 2023 19:11:59 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 19:12:00 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 19:12:00 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Wed, 03 May 2023 19:13:28 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 19:13:28 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 19:13:28 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 19:13:28 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 19:13:28 GMT
EXPOSE 443
# Wed, 03 May 2023 19:13:29 GMT
CMD []
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f09fd0d72136410c7ad5b51c26522f83cd759a0379e5816e924e2608485b8e`  
		Last Modified: Wed, 03 May 2023 19:13:57 GMT  
		Size: 1.6 MB (1605949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80168d86b1303babc0093dced4b43378e6fdf51f44c4dba97b4903955a4dd696`  
		Last Modified: Wed, 03 May 2023 19:13:57 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; 386

```console
$ docker pull hitch@sha256:1784bb3cc90a04b9f1d0d7b12716b0fac39220ff87baf5421fe0b162cbec05cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34018056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abff1422a0f763175c425a62e087f08e5e7fead9287ddbf945845e161b01f6c`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:39:30 GMT
ADD file:8319fc1c1a3c0f2a6bb03636fe1fd0eb7fa52c58505d279e4366627452ea2104 in / 
# Tue, 23 May 2023 00:39:30 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:21:11 GMT
ARG SRCVER=1.7.2
# Tue, 23 May 2023 02:21:11 GMT
ARG PKGVER=1
# Tue, 23 May 2023 02:21:11 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 02:21:11 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 02:21:11 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 23 May 2023 02:23:04 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 02:23:04 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 02:23:04 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 02:23:04 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 02:23:05 GMT
EXPOSE 443
# Tue, 23 May 2023 02:23:05 GMT
CMD []
```

-	Layers:
	-	`sha256:0f5d158483bd0ffef0c106b68514aece2ca0500d2990c830844277cbca7fe0bc`  
		Last Modified: Tue, 23 May 2023 00:44:28 GMT  
		Size: 32.4 MB (32388165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fa083c96300d2c89bd9171730144af8aca582a16d163c2cb8ed1cb29b385d3`  
		Last Modified: Tue, 23 May 2023 02:23:40 GMT  
		Size: 1.6 MB (1629475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf00415e113963832d912f35449fdae3f2c51b4cae619d784b85fe2801aa53a`  
		Last Modified: Tue, 23 May 2023 02:23:40 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; ppc64le

```console
$ docker pull hitch@sha256:6fa2699833f96d0bc0c1edb3aaff29fe319d3845b856020147cd4ca1d12b83b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36966506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767a07bd307569ab11622655b901ea76a114c019b3823388b4ee3a9a4b0db7ce`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 01:17:35 GMT
ADD file:719aea085739ec41c255f35070ca652d4e356c5ee62c8237f8ebc7389feb8e38 in / 
# Tue, 23 May 2023 01:17:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:01:53 GMT
ARG SRCVER=1.7.2
# Tue, 23 May 2023 04:01:54 GMT
ARG PKGVER=1
# Tue, 23 May 2023 04:01:54 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 04:01:54 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 04:01:54 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 23 May 2023 04:06:03 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 04:06:04 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 04:06:04 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 04:06:04 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 04:06:04 GMT
EXPOSE 443
# Tue, 23 May 2023 04:06:05 GMT
CMD []
```

-	Layers:
	-	`sha256:b6c83d2f160e7e38990586d26caa105ff577368a887fd754ae4634cdbfec83ff`  
		Last Modified: Tue, 23 May 2023 01:22:03 GMT  
		Size: 35.3 MB (35280911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaca712bf76fbe2f0a6242f971a33bdb3316269b568a83adbb9f257ed45fedc`  
		Last Modified: Tue, 23 May 2023 04:06:41 GMT  
		Size: 1.7 MB (1685177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba7766ef7f2592880167519133ffc0f376c44f67646d20140d73cc2e76f7d9d`  
		Last Modified: Tue, 23 May 2023 04:06:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; s390x

```console
$ docker pull hitch@sha256:63a4dd3d3a66996e3f653d23831157dc75695213bc33ce7c8e65951c5645ff2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31263978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d9a1a06b511b02a6231b2a11714620be250fcef957eedcc58f2be222f55754`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:42:52 GMT
ADD file:23b1e12559302529556a94a1d4098dbdb454e263265258b940c2b2d23a97c121 in / 
# Tue, 23 May 2023 00:42:54 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:28:52 GMT
ARG SRCVER=1.7.2
# Tue, 23 May 2023 03:28:52 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:28:52 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:28:52 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:28:53 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 23 May 2023 03:30:13 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 03:30:13 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 03:30:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 03:30:13 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 03:30:13 GMT
EXPOSE 443
# Tue, 23 May 2023 03:30:13 GMT
CMD []
```

-	Layers:
	-	`sha256:9c24ec455bdb6a9ad0d033c7cce8e71dd5bdbbe53a86d5feeb8d4cb7804fb8e5`  
		Last Modified: Tue, 23 May 2023 00:45:47 GMT  
		Size: 29.6 MB (29642170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7de11580e1879b459dbeefc114ada2b442f0f2a5ff5ee82fe86bb399fd572`  
		Last Modified: Tue, 23 May 2023 03:30:41 GMT  
		Size: 1.6 MB (1621391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd34c028b72ea8e1036059d23e0471f102c0868dc2c2eaee4af3a2bf430bffe`  
		Last Modified: Tue, 23 May 2023 03:30:41 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.3`

```console
$ docker pull hitch@sha256:d51d99b186aade9dd4830ffe2da37530750a2f75e07f0767f67f46ba1f5d3b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.7.3` - linux; amd64

```console
$ docker pull hitch@sha256:ca330d657f8c093a47de0a3fa1fac6de63e910c0d4c0fb4e3b31a3bcee4a92bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33029490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565dce13d52a485bf741af18a4b7ba34bcb5116aa517f9979f6bd772d1a9e14d`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:42:42 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 20:42:42 GMT
ARG PKGVER=1
# Wed, 03 May 2023 20:42:42 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 20:42:42 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 20:42:42 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 20:45:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 20:45:00 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 20:45:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 20:45:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 20:45:00 GMT
EXPOSE 443
# Wed, 03 May 2023 20:45:00 GMT
CMD []
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5068fb84d96c68410d2be20fc4225f48dfa270dbc5b30b989f758f1ad5321d29`  
		Last Modified: Wed, 03 May 2023 20:47:06 GMT  
		Size: 1.6 MB (1625559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536fe63701960687ec7375f35e1c4a462045d6268be880184143f7a144bfb5f9`  
		Last Modified: Wed, 03 May 2023 20:47:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; arm variant v7

```console
$ docker pull hitch@sha256:bfe06ecd7baf8664063dafabfc67269e5c08fa2beee60045ca63da7d29cceb0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28109984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e80e6f4b4ac0406b6e6f3a596a00212adf2d771ea6830a6200e654270058a1`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:24:57 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 22:24:57 GMT
ARG PKGVER=1
# Wed, 03 May 2023 22:24:57 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 22:24:57 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 22:24:58 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 22:27:03 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 22:27:03 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 22:27:03 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 22:27:03 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 22:27:03 GMT
EXPOSE 443
# Wed, 03 May 2023 22:27:04 GMT
CMD []
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2dab1babd812b56d3e886093fe502a9104e86360c036925512f64fcf5f32e`  
		Last Modified: Wed, 03 May 2023 22:29:18 GMT  
		Size: 1.5 MB (1544920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09219df1ddb6a679b8ab5b0526ed93731bd464ef8bbb80ef08d367f2fe3ef70`  
		Last Modified: Wed, 03 May 2023 22:29:18 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:d1629f7d56021774230df5c34e353f7ac5e49b62644c4cc0066d318e4bd96c0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31659894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0fafc9d733edf9dba64b5b95814ca46540fbbb9f0dc3ef52d94315fd3e1bef`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:09:07 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 19:09:07 GMT
ARG PKGVER=1
# Wed, 03 May 2023 19:09:07 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 19:09:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 19:09:07 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 19:11:45 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 19:11:45 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 19:11:45 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 19:11:45 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 19:11:45 GMT
EXPOSE 443
# Wed, 03 May 2023 19:11:46 GMT
CMD []
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d452d8d83439efc46c6b37fed2cd2d54812801e1178d7c34fbb3080634fc529f`  
		Last Modified: Wed, 03 May 2023 19:13:44 GMT  
		Size: 1.6 MB (1606744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2260a81f4103e7411fa7d44f9e74200073c0bcd4c91c1bbc262db1218729be27`  
		Last Modified: Wed, 03 May 2023 19:13:44 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; 386

```console
$ docker pull hitch@sha256:8038ee914449710b1c88c0717c219a01a14290adeddf269e10ed92fcd84a9a79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34019411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f6718679c908b2e1555f63d337f2c20d2889a7c7a41f936566de2722f0b594`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:39:30 GMT
ADD file:8319fc1c1a3c0f2a6bb03636fe1fd0eb7fa52c58505d279e4366627452ea2104 in / 
# Tue, 23 May 2023 00:39:30 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:17:48 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 02:17:48 GMT
ARG PKGVER=1
# Tue, 23 May 2023 02:17:48 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 02:17:48 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 02:17:49 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 02:20:55 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 02:20:55 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 02:20:55 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 02:20:55 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 02:20:55 GMT
EXPOSE 443
# Tue, 23 May 2023 02:20:55 GMT
CMD []
```

-	Layers:
	-	`sha256:0f5d158483bd0ffef0c106b68514aece2ca0500d2990c830844277cbca7fe0bc`  
		Last Modified: Tue, 23 May 2023 00:44:28 GMT  
		Size: 32.4 MB (32388165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0552cf37dffe35777a972a2fbfdb0261a9dab866e16b0cbc255be1ea4ac1ce93`  
		Last Modified: Tue, 23 May 2023 02:23:26 GMT  
		Size: 1.6 MB (1630829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab59e29f2218e25e27a6bfe94a5e89f0a3072361f36219c75fb7ab081c755ed`  
		Last Modified: Tue, 23 May 2023 02:23:26 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; ppc64le

```console
$ docker pull hitch@sha256:e9b5286e8e0bc3ccfc33c9349e6b63a803321e5363dd87a10448da6c48f5ef9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36967394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef237ebe0340d5c57ca79403a2a8fb0185b42d9f8b985263ad6c1466989494d4`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 01:17:35 GMT
ADD file:719aea085739ec41c255f35070ca652d4e356c5ee62c8237f8ebc7389feb8e38 in / 
# Tue, 23 May 2023 01:17:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:56:44 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 03:56:44 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:56:45 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:56:45 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:56:48 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 04:01:36 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 04:01:36 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 04:01:36 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 04:01:37 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 04:01:37 GMT
EXPOSE 443
# Tue, 23 May 2023 04:01:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b6c83d2f160e7e38990586d26caa105ff577368a887fd754ae4634cdbfec83ff`  
		Last Modified: Tue, 23 May 2023 01:22:03 GMT  
		Size: 35.3 MB (35280911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025635a981d45424d281e8d94eb0ddf5ebf5079200c85ba9948aea42baa0c32b`  
		Last Modified: Tue, 23 May 2023 04:06:26 GMT  
		Size: 1.7 MB (1686066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1445e943c8f14237987563f07add91ea058e5529a487ecf009b2b08e6a756e`  
		Last Modified: Tue, 23 May 2023 04:06:25 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; s390x

```console
$ docker pull hitch@sha256:12e21419e43bbf8ff6e18c60fadc7404b20bd3e3f026df5ff56059c9e1f7175c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31264475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dee568490617674e36ccb727444753eae5a02daeb977d2bebe375f21acfba27`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:42:52 GMT
ADD file:23b1e12559302529556a94a1d4098dbdb454e263265258b940c2b2d23a97c121 in / 
# Tue, 23 May 2023 00:42:54 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:27:20 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 03:27:20 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:27:20 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:27:20 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:27:20 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 03:28:40 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 03:28:40 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 03:28:40 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 03:28:40 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 03:28:40 GMT
EXPOSE 443
# Tue, 23 May 2023 03:28:40 GMT
CMD []
```

-	Layers:
	-	`sha256:9c24ec455bdb6a9ad0d033c7cce8e71dd5bdbbe53a86d5feeb8d4cb7804fb8e5`  
		Last Modified: Tue, 23 May 2023 00:45:47 GMT  
		Size: 29.6 MB (29642170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfffa71d72401278590e0bd1d1629aabea25dc2c971d63c00a8acace2d1877a0`  
		Last Modified: Tue, 23 May 2023 03:30:33 GMT  
		Size: 1.6 MB (1621889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb2959ffed3113cab3c7f0e0e8144cde4bbb0efbf393fc7a5b7d4908dcaf07`  
		Last Modified: Tue, 23 May 2023 03:30:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.3-1`

```console
$ docker pull hitch@sha256:d51d99b186aade9dd4830ffe2da37530750a2f75e07f0767f67f46ba1f5d3b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.7.3-1` - linux; amd64

```console
$ docker pull hitch@sha256:ca330d657f8c093a47de0a3fa1fac6de63e910c0d4c0fb4e3b31a3bcee4a92bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33029490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565dce13d52a485bf741af18a4b7ba34bcb5116aa517f9979f6bd772d1a9e14d`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:42:42 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 20:42:42 GMT
ARG PKGVER=1
# Wed, 03 May 2023 20:42:42 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 20:42:42 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 20:42:42 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 20:45:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 20:45:00 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 20:45:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 20:45:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 20:45:00 GMT
EXPOSE 443
# Wed, 03 May 2023 20:45:00 GMT
CMD []
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5068fb84d96c68410d2be20fc4225f48dfa270dbc5b30b989f758f1ad5321d29`  
		Last Modified: Wed, 03 May 2023 20:47:06 GMT  
		Size: 1.6 MB (1625559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536fe63701960687ec7375f35e1c4a462045d6268be880184143f7a144bfb5f9`  
		Last Modified: Wed, 03 May 2023 20:47:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:bfe06ecd7baf8664063dafabfc67269e5c08fa2beee60045ca63da7d29cceb0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28109984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e80e6f4b4ac0406b6e6f3a596a00212adf2d771ea6830a6200e654270058a1`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:24:57 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 22:24:57 GMT
ARG PKGVER=1
# Wed, 03 May 2023 22:24:57 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 22:24:57 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 22:24:58 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 22:27:03 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 22:27:03 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 22:27:03 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 22:27:03 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 22:27:03 GMT
EXPOSE 443
# Wed, 03 May 2023 22:27:04 GMT
CMD []
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2dab1babd812b56d3e886093fe502a9104e86360c036925512f64fcf5f32e`  
		Last Modified: Wed, 03 May 2023 22:29:18 GMT  
		Size: 1.5 MB (1544920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09219df1ddb6a679b8ab5b0526ed93731bd464ef8bbb80ef08d367f2fe3ef70`  
		Last Modified: Wed, 03 May 2023 22:29:18 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:d1629f7d56021774230df5c34e353f7ac5e49b62644c4cc0066d318e4bd96c0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31659894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0fafc9d733edf9dba64b5b95814ca46540fbbb9f0dc3ef52d94315fd3e1bef`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:09:07 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 19:09:07 GMT
ARG PKGVER=1
# Wed, 03 May 2023 19:09:07 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 19:09:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 19:09:07 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 19:11:45 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 19:11:45 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 19:11:45 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 19:11:45 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 19:11:45 GMT
EXPOSE 443
# Wed, 03 May 2023 19:11:46 GMT
CMD []
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d452d8d83439efc46c6b37fed2cd2d54812801e1178d7c34fbb3080634fc529f`  
		Last Modified: Wed, 03 May 2023 19:13:44 GMT  
		Size: 1.6 MB (1606744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2260a81f4103e7411fa7d44f9e74200073c0bcd4c91c1bbc262db1218729be27`  
		Last Modified: Wed, 03 May 2023 19:13:44 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; 386

```console
$ docker pull hitch@sha256:8038ee914449710b1c88c0717c219a01a14290adeddf269e10ed92fcd84a9a79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34019411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f6718679c908b2e1555f63d337f2c20d2889a7c7a41f936566de2722f0b594`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:39:30 GMT
ADD file:8319fc1c1a3c0f2a6bb03636fe1fd0eb7fa52c58505d279e4366627452ea2104 in / 
# Tue, 23 May 2023 00:39:30 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:17:48 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 02:17:48 GMT
ARG PKGVER=1
# Tue, 23 May 2023 02:17:48 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 02:17:48 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 02:17:49 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 02:20:55 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 02:20:55 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 02:20:55 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 02:20:55 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 02:20:55 GMT
EXPOSE 443
# Tue, 23 May 2023 02:20:55 GMT
CMD []
```

-	Layers:
	-	`sha256:0f5d158483bd0ffef0c106b68514aece2ca0500d2990c830844277cbca7fe0bc`  
		Last Modified: Tue, 23 May 2023 00:44:28 GMT  
		Size: 32.4 MB (32388165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0552cf37dffe35777a972a2fbfdb0261a9dab866e16b0cbc255be1ea4ac1ce93`  
		Last Modified: Tue, 23 May 2023 02:23:26 GMT  
		Size: 1.6 MB (1630829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab59e29f2218e25e27a6bfe94a5e89f0a3072361f36219c75fb7ab081c755ed`  
		Last Modified: Tue, 23 May 2023 02:23:26 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; ppc64le

```console
$ docker pull hitch@sha256:e9b5286e8e0bc3ccfc33c9349e6b63a803321e5363dd87a10448da6c48f5ef9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36967394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef237ebe0340d5c57ca79403a2a8fb0185b42d9f8b985263ad6c1466989494d4`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 01:17:35 GMT
ADD file:719aea085739ec41c255f35070ca652d4e356c5ee62c8237f8ebc7389feb8e38 in / 
# Tue, 23 May 2023 01:17:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:56:44 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 03:56:44 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:56:45 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:56:45 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:56:48 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 04:01:36 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 04:01:36 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 04:01:36 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 04:01:37 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 04:01:37 GMT
EXPOSE 443
# Tue, 23 May 2023 04:01:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b6c83d2f160e7e38990586d26caa105ff577368a887fd754ae4634cdbfec83ff`  
		Last Modified: Tue, 23 May 2023 01:22:03 GMT  
		Size: 35.3 MB (35280911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025635a981d45424d281e8d94eb0ddf5ebf5079200c85ba9948aea42baa0c32b`  
		Last Modified: Tue, 23 May 2023 04:06:26 GMT  
		Size: 1.7 MB (1686066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1445e943c8f14237987563f07add91ea058e5529a487ecf009b2b08e6a756e`  
		Last Modified: Tue, 23 May 2023 04:06:25 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; s390x

```console
$ docker pull hitch@sha256:12e21419e43bbf8ff6e18c60fadc7404b20bd3e3f026df5ff56059c9e1f7175c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31264475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dee568490617674e36ccb727444753eae5a02daeb977d2bebe375f21acfba27`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:42:52 GMT
ADD file:23b1e12559302529556a94a1d4098dbdb454e263265258b940c2b2d23a97c121 in / 
# Tue, 23 May 2023 00:42:54 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:27:20 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 03:27:20 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:27:20 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:27:20 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:27:20 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 03:28:40 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 03:28:40 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 03:28:40 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 03:28:40 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 03:28:40 GMT
EXPOSE 443
# Tue, 23 May 2023 03:28:40 GMT
CMD []
```

-	Layers:
	-	`sha256:9c24ec455bdb6a9ad0d033c7cce8e71dd5bdbbe53a86d5feeb8d4cb7804fb8e5`  
		Last Modified: Tue, 23 May 2023 00:45:47 GMT  
		Size: 29.6 MB (29642170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfffa71d72401278590e0bd1d1629aabea25dc2c971d63c00a8acace2d1877a0`  
		Last Modified: Tue, 23 May 2023 03:30:33 GMT  
		Size: 1.6 MB (1621889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb2959ffed3113cab3c7f0e0e8144cde4bbb0efbf393fc7a5b7d4908dcaf07`  
		Last Modified: Tue, 23 May 2023 03:30:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:latest`

```console
$ docker pull hitch@sha256:d51d99b186aade9dd4830ffe2da37530750a2f75e07f0767f67f46ba1f5d3b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:latest` - linux; amd64

```console
$ docker pull hitch@sha256:ca330d657f8c093a47de0a3fa1fac6de63e910c0d4c0fb4e3b31a3bcee4a92bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33029490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565dce13d52a485bf741af18a4b7ba34bcb5116aa517f9979f6bd772d1a9e14d`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:42:42 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 20:42:42 GMT
ARG PKGVER=1
# Wed, 03 May 2023 20:42:42 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 20:42:42 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 20:42:42 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 20:45:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 20:45:00 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 20:45:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 20:45:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 20:45:00 GMT
EXPOSE 443
# Wed, 03 May 2023 20:45:00 GMT
CMD []
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5068fb84d96c68410d2be20fc4225f48dfa270dbc5b30b989f758f1ad5321d29`  
		Last Modified: Wed, 03 May 2023 20:47:06 GMT  
		Size: 1.6 MB (1625559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536fe63701960687ec7375f35e1c4a462045d6268be880184143f7a144bfb5f9`  
		Last Modified: Wed, 03 May 2023 20:47:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:bfe06ecd7baf8664063dafabfc67269e5c08fa2beee60045ca63da7d29cceb0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28109984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e80e6f4b4ac0406b6e6f3a596a00212adf2d771ea6830a6200e654270058a1`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:24:57 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 22:24:57 GMT
ARG PKGVER=1
# Wed, 03 May 2023 22:24:57 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 22:24:57 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 22:24:58 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 22:27:03 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 22:27:03 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 22:27:03 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 22:27:03 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 22:27:03 GMT
EXPOSE 443
# Wed, 03 May 2023 22:27:04 GMT
CMD []
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2dab1babd812b56d3e886093fe502a9104e86360c036925512f64fcf5f32e`  
		Last Modified: Wed, 03 May 2023 22:29:18 GMT  
		Size: 1.5 MB (1544920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09219df1ddb6a679b8ab5b0526ed93731bd464ef8bbb80ef08d367f2fe3ef70`  
		Last Modified: Wed, 03 May 2023 22:29:18 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:d1629f7d56021774230df5c34e353f7ac5e49b62644c4cc0066d318e4bd96c0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31659894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0fafc9d733edf9dba64b5b95814ca46540fbbb9f0dc3ef52d94315fd3e1bef`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:09:07 GMT
ARG SRCVER=1.7.3
# Wed, 03 May 2023 19:09:07 GMT
ARG PKGVER=1
# Wed, 03 May 2023 19:09:07 GMT
ARG DISTVER=bullseye
# Wed, 03 May 2023 19:09:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 03 May 2023 19:09:07 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 03 May 2023 19:11:45 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 03 May 2023 19:11:45 GMT
WORKDIR /etc/hitch
# Wed, 03 May 2023 19:11:45 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 03 May 2023 19:11:45 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 03 May 2023 19:11:45 GMT
EXPOSE 443
# Wed, 03 May 2023 19:11:46 GMT
CMD []
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d452d8d83439efc46c6b37fed2cd2d54812801e1178d7c34fbb3080634fc529f`  
		Last Modified: Wed, 03 May 2023 19:13:44 GMT  
		Size: 1.6 MB (1606744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2260a81f4103e7411fa7d44f9e74200073c0bcd4c91c1bbc262db1218729be27`  
		Last Modified: Wed, 03 May 2023 19:13:44 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:8038ee914449710b1c88c0717c219a01a14290adeddf269e10ed92fcd84a9a79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34019411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f6718679c908b2e1555f63d337f2c20d2889a7c7a41f936566de2722f0b594`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:39:30 GMT
ADD file:8319fc1c1a3c0f2a6bb03636fe1fd0eb7fa52c58505d279e4366627452ea2104 in / 
# Tue, 23 May 2023 00:39:30 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:17:48 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 02:17:48 GMT
ARG PKGVER=1
# Tue, 23 May 2023 02:17:48 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 02:17:48 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 02:17:49 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 02:20:55 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 02:20:55 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 02:20:55 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 02:20:55 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 02:20:55 GMT
EXPOSE 443
# Tue, 23 May 2023 02:20:55 GMT
CMD []
```

-	Layers:
	-	`sha256:0f5d158483bd0ffef0c106b68514aece2ca0500d2990c830844277cbca7fe0bc`  
		Last Modified: Tue, 23 May 2023 00:44:28 GMT  
		Size: 32.4 MB (32388165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0552cf37dffe35777a972a2fbfdb0261a9dab866e16b0cbc255be1ea4ac1ce93`  
		Last Modified: Tue, 23 May 2023 02:23:26 GMT  
		Size: 1.6 MB (1630829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab59e29f2218e25e27a6bfe94a5e89f0a3072361f36219c75fb7ab081c755ed`  
		Last Modified: Tue, 23 May 2023 02:23:26 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; ppc64le

```console
$ docker pull hitch@sha256:e9b5286e8e0bc3ccfc33c9349e6b63a803321e5363dd87a10448da6c48f5ef9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36967394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef237ebe0340d5c57ca79403a2a8fb0185b42d9f8b985263ad6c1466989494d4`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 01:17:35 GMT
ADD file:719aea085739ec41c255f35070ca652d4e356c5ee62c8237f8ebc7389feb8e38 in / 
# Tue, 23 May 2023 01:17:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:56:44 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 03:56:44 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:56:45 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:56:45 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:56:48 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 04:01:36 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 04:01:36 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 04:01:36 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 04:01:37 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 04:01:37 GMT
EXPOSE 443
# Tue, 23 May 2023 04:01:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b6c83d2f160e7e38990586d26caa105ff577368a887fd754ae4634cdbfec83ff`  
		Last Modified: Tue, 23 May 2023 01:22:03 GMT  
		Size: 35.3 MB (35280911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025635a981d45424d281e8d94eb0ddf5ebf5079200c85ba9948aea42baa0c32b`  
		Last Modified: Tue, 23 May 2023 04:06:26 GMT  
		Size: 1.7 MB (1686066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1445e943c8f14237987563f07add91ea058e5529a487ecf009b2b08e6a756e`  
		Last Modified: Tue, 23 May 2023 04:06:25 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; s390x

```console
$ docker pull hitch@sha256:12e21419e43bbf8ff6e18c60fadc7404b20bd3e3f026df5ff56059c9e1f7175c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31264475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dee568490617674e36ccb727444753eae5a02daeb977d2bebe375f21acfba27`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 May 2023 00:42:52 GMT
ADD file:23b1e12559302529556a94a1d4098dbdb454e263265258b940c2b2d23a97c121 in / 
# Tue, 23 May 2023 00:42:54 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:27:20 GMT
ARG SRCVER=1.7.3
# Tue, 23 May 2023 03:27:20 GMT
ARG PKGVER=1
# Tue, 23 May 2023 03:27:20 GMT
ARG DISTVER=bullseye
# Tue, 23 May 2023 03:27:20 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 23 May 2023 03:27:20 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 23 May 2023 03:28:40 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 23 May 2023 03:28:40 GMT
WORKDIR /etc/hitch
# Tue, 23 May 2023 03:28:40 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 23 May 2023 03:28:40 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 23 May 2023 03:28:40 GMT
EXPOSE 443
# Tue, 23 May 2023 03:28:40 GMT
CMD []
```

-	Layers:
	-	`sha256:9c24ec455bdb6a9ad0d033c7cce8e71dd5bdbbe53a86d5feeb8d4cb7804fb8e5`  
		Last Modified: Tue, 23 May 2023 00:45:47 GMT  
		Size: 29.6 MB (29642170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfffa71d72401278590e0bd1d1629aabea25dc2c971d63c00a8acace2d1877a0`  
		Last Modified: Tue, 23 May 2023 03:30:33 GMT  
		Size: 1.6 MB (1621889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb2959ffed3113cab3c7f0e0e8144cde4bbb0efbf393fc7a5b7d4908dcaf07`  
		Last Modified: Tue, 23 May 2023 03:30:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
