<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.8`](#varnish608)
-	[`varnish:6.6`](#varnish66)
-	[`varnish:6.6-alpine`](#varnish66-alpine)
-	[`varnish:6.6.1`](#varnish661)
-	[`varnish:6.6.1-alpine`](#varnish661-alpine)
-	[`varnish:7.0`](#varnish70)
-	[`varnish:7.0-alpine`](#varnish70-alpine)
-	[`varnish:7.0.1`](#varnish701)
-	[`varnish:7.0.1-alpine`](#varnish701-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:99de3ef66b51471e325b98d806e4589382c8067970027968cb8ab254fbfae161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:f1b99a76e21fcc1d5098783f161e5d8baae9f14a6b08b8210931415e7b413aec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100572810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aecc682cab2e96109a6d0ef8391b93f2f4ba92ce2b61702096dcf3fb8a5057`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:02:38 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:29:34 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 29 Nov 2021 18:29:34 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:29:35 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:29:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:29:35 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:29:35 GMT
CMD []
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd5a37ea8efe8f63cfc190a6128c5a382c13f7f68e6c37fe345ff78861a2553`  
		Last Modified: Mon, 29 Nov 2021 18:31:41 GMT  
		Size: 69.2 MB (69201839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d24281ccd4f88407de3ba98d9b6ff1a1d7cfc33c3e1326a6ac4902b571d82df`  
		Last Modified: Mon, 29 Nov 2021 18:31:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c07401fbada8dcfb30316530b22680d446cb206090d92fe1530bc8244876d941
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80045960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0575bdb28c3e85f2bec56215667be87aed7cf9da82997ae6cf0388b9920d5c3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 09:52:16 GMT
ENV VARNISH_SIZE=100M
# Thu, 18 Nov 2021 10:05:04 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 18 Nov 2021 10:05:05 GMT
WORKDIR /etc/varnish
# Thu, 18 Nov 2021 10:05:05 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 18 Nov 2021 10:05:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 18 Nov 2021 10:05:06 GMT
EXPOSE 80 8443
# Thu, 18 Nov 2021 10:05:07 GMT
CMD []
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5736611207f9ab6e495c3a8258205db6cf5c8dd58bbba8cf9058a1c3271b70c5`  
		Last Modified: Thu, 18 Nov 2021 10:07:47 GMT  
		Size: 53.5 MB (53472100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b70a0546c868480d128124ce89dc7923b8ce3979c92d7887f34cbc043b2267e`  
		Last Modified: Thu, 18 Nov 2021 10:07:19 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c928b550c26640919c0582045590d449f8ed4dde96d2aef96b9cc7c9ed409530
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97533085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04aad97694b8ac0c6fad4a40b9f56be76415697bd3c21381e912650779452d92`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:32:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 04:39:46 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 04:39:46 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 04:39:48 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 04:39:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 04:39:49 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 04:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ccc34b59256b34a663b30483f48ffe180875b7b9ab652ca6c5f086239106d2`  
		Last Modified: Wed, 17 Nov 2021 04:41:37 GMT  
		Size: 67.5 MB (67475863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ee133477d1347e016652a50cf39a47c1d9b619e1bcdbaefe5f26097572c7d9`  
		Last Modified: Wed, 17 Nov 2021 04:41:27 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:5d755ac59fca0f6e2c886e91cd66e4a1c18fbf9f67acd0ad7da6ebd23c2f8288
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104751828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90279c337e591d81685afdb3579485a9d53623da5cbd404029951f6901d0f1ab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:10:10 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 03:17:14 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 03:17:17 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 03:17:17 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 03:17:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 03:17:18 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 03:17:18 GMT
CMD []
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cff288a3cfecf3065cb555da4033fd5136fa00c1d1a3fbaf2d26d86a654a042`  
		Last Modified: Wed, 17 Nov 2021 03:18:50 GMT  
		Size: 72.4 MB (72370444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b900b861bf9ebaa2a7a820a6b65a8e534f39d694b28f38933e74e384026298cf`  
		Last Modified: Wed, 17 Nov 2021 03:18:35 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:40cf090fa2b141c82b92a97999cb6e5edabfd8ca85ba937bd9d7b3634ce3f4bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102651397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591e633f06d21eec5a59ce9510e2695cc4082370f3d317fbed87d9c6713794d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:04:25 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 07:36:01 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 07:36:07 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 07:36:08 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 07:36:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 07:36:11 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 07:36:14 GMT
CMD []
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd72144f4cad756c9443b3fe38a48bb132072f786b8b8cf5dd94d6aac00175f6`  
		Last Modified: Wed, 17 Nov 2021 07:38:13 GMT  
		Size: 67.4 MB (67379313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26b3cef66f6a2e490527b4897674457868ceb0a192e3f9876834133cbcede80`  
		Last Modified: Wed, 17 Nov 2021 07:38:00 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:70f2c1561bd91312529d25d9060d1b6023f1e97a5d843a0af53f66845a91fcd4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83786925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d59abd0994117eb46de293abdc871becc1c4e79fa1e2a7177865c1066f96ec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:09:56 GMT
ENV VARNISH_SIZE=100M
# Wed, 24 Nov 2021 20:29:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 24 Nov 2021 20:29:50 GMT
WORKDIR /etc/varnish
# Wed, 24 Nov 2021 20:29:50 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 24 Nov 2021 20:29:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 24 Nov 2021 20:29:50 GMT
EXPOSE 80 8443
# Wed, 24 Nov 2021 20:29:51 GMT
CMD []
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10c09fdaf917d59b135390e666871ffe70e2701d0e957686bdef300d8ccc837`  
		Last Modified: Wed, 24 Nov 2021 20:31:20 GMT  
		Size: 54.1 MB (54135264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e37af7af0efec3cdee9c3eaf78d448e442ebd292bd854fd2227521f177558b3`  
		Last Modified: Wed, 24 Nov 2021 20:31:13 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.8`

```console
$ docker pull varnish@sha256:99de3ef66b51471e325b98d806e4589382c8067970027968cb8ab254fbfae161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.0.8` - linux; amd64

```console
$ docker pull varnish@sha256:f1b99a76e21fcc1d5098783f161e5d8baae9f14a6b08b8210931415e7b413aec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100572810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aecc682cab2e96109a6d0ef8391b93f2f4ba92ce2b61702096dcf3fb8a5057`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:02:38 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:29:34 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 29 Nov 2021 18:29:34 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:29:35 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:29:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:29:35 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:29:35 GMT
CMD []
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd5a37ea8efe8f63cfc190a6128c5a382c13f7f68e6c37fe345ff78861a2553`  
		Last Modified: Mon, 29 Nov 2021 18:31:41 GMT  
		Size: 69.2 MB (69201839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d24281ccd4f88407de3ba98d9b6ff1a1d7cfc33c3e1326a6ac4902b571d82df`  
		Last Modified: Mon, 29 Nov 2021 18:31:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.8` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c07401fbada8dcfb30316530b22680d446cb206090d92fe1530bc8244876d941
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80045960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0575bdb28c3e85f2bec56215667be87aed7cf9da82997ae6cf0388b9920d5c3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 09:52:16 GMT
ENV VARNISH_SIZE=100M
# Thu, 18 Nov 2021 10:05:04 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 18 Nov 2021 10:05:05 GMT
WORKDIR /etc/varnish
# Thu, 18 Nov 2021 10:05:05 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 18 Nov 2021 10:05:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 18 Nov 2021 10:05:06 GMT
EXPOSE 80 8443
# Thu, 18 Nov 2021 10:05:07 GMT
CMD []
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5736611207f9ab6e495c3a8258205db6cf5c8dd58bbba8cf9058a1c3271b70c5`  
		Last Modified: Thu, 18 Nov 2021 10:07:47 GMT  
		Size: 53.5 MB (53472100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b70a0546c868480d128124ce89dc7923b8ce3979c92d7887f34cbc043b2267e`  
		Last Modified: Thu, 18 Nov 2021 10:07:19 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c928b550c26640919c0582045590d449f8ed4dde96d2aef96b9cc7c9ed409530
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97533085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04aad97694b8ac0c6fad4a40b9f56be76415697bd3c21381e912650779452d92`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:32:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 04:39:46 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 04:39:46 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 04:39:48 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 04:39:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 04:39:49 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 04:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ccc34b59256b34a663b30483f48ffe180875b7b9ab652ca6c5f086239106d2`  
		Last Modified: Wed, 17 Nov 2021 04:41:37 GMT  
		Size: 67.5 MB (67475863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ee133477d1347e016652a50cf39a47c1d9b619e1bcdbaefe5f26097572c7d9`  
		Last Modified: Wed, 17 Nov 2021 04:41:27 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.8` - linux; 386

```console
$ docker pull varnish@sha256:5d755ac59fca0f6e2c886e91cd66e4a1c18fbf9f67acd0ad7da6ebd23c2f8288
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104751828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90279c337e591d81685afdb3579485a9d53623da5cbd404029951f6901d0f1ab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:10:10 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 03:17:14 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 03:17:17 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 03:17:17 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 03:17:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 03:17:18 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 03:17:18 GMT
CMD []
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cff288a3cfecf3065cb555da4033fd5136fa00c1d1a3fbaf2d26d86a654a042`  
		Last Modified: Wed, 17 Nov 2021 03:18:50 GMT  
		Size: 72.4 MB (72370444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b900b861bf9ebaa2a7a820a6b65a8e534f39d694b28f38933e74e384026298cf`  
		Last Modified: Wed, 17 Nov 2021 03:18:35 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.8` - linux; ppc64le

```console
$ docker pull varnish@sha256:40cf090fa2b141c82b92a97999cb6e5edabfd8ca85ba937bd9d7b3634ce3f4bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102651397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591e633f06d21eec5a59ce9510e2695cc4082370f3d317fbed87d9c6713794d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:04:25 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 07:36:01 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 07:36:07 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 07:36:08 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 07:36:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 07:36:11 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 07:36:14 GMT
CMD []
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd72144f4cad756c9443b3fe38a48bb132072f786b8b8cf5dd94d6aac00175f6`  
		Last Modified: Wed, 17 Nov 2021 07:38:13 GMT  
		Size: 67.4 MB (67379313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26b3cef66f6a2e490527b4897674457868ceb0a192e3f9876834133cbcede80`  
		Last Modified: Wed, 17 Nov 2021 07:38:00 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.8` - linux; s390x

```console
$ docker pull varnish@sha256:70f2c1561bd91312529d25d9060d1b6023f1e97a5d843a0af53f66845a91fcd4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83786925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d59abd0994117eb46de293abdc871becc1c4e79fa1e2a7177865c1066f96ec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:09:56 GMT
ENV VARNISH_SIZE=100M
# Wed, 24 Nov 2021 20:29:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 24 Nov 2021 20:29:50 GMT
WORKDIR /etc/varnish
# Wed, 24 Nov 2021 20:29:50 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 24 Nov 2021 20:29:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 24 Nov 2021 20:29:50 GMT
EXPOSE 80 8443
# Wed, 24 Nov 2021 20:29:51 GMT
CMD []
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10c09fdaf917d59b135390e666871ffe70e2701d0e957686bdef300d8ccc837`  
		Last Modified: Wed, 24 Nov 2021 20:31:20 GMT  
		Size: 54.1 MB (54135264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e37af7af0efec3cdee9c3eaf78d448e442ebd292bd854fd2227521f177558b3`  
		Last Modified: Wed, 24 Nov 2021 20:31:13 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6`

```console
$ docker pull varnish@sha256:d97bb2325f93e8f11840ec5dbbecfbe0f6eafe3c65065282812dfe818490f56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.6` - linux; amd64

```console
$ docker pull varnish@sha256:14dc4591ca6ebc682192aeb88279148038ba1c80199db6734fd1ed3d9fe82ae1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101111708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9e2d7a898d88289a0dcaec28a767b263f436d22f9af49b303d94a3f22c9bcf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:02:38 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:26:15 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 29 Nov 2021 18:26:16 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:26:16 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:26:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:26:17 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:26:17 GMT
CMD []
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55795befb5cc32412c795a50fd294ec6bb72c993f58f3aa1e6aeb4b2632c353`  
		Last Modified: Mon, 29 Nov 2021 18:30:57 GMT  
		Size: 69.7 MB (69740739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74423f9b842a246e5b4d79beea3320392f0a3c0d50409eee98d13a45f799d6cc`  
		Last Modified: Mon, 29 Nov 2021 18:30:48 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:413095e503ec1943459aceac4700c136814ec9e17b0059fde00ac9f076071fe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80972534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f48b7cb9ce5481ed2e6b0ee90f2780f7772aa25e665040cdad90f309261a31`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 09:52:16 GMT
ENV VARNISH_SIZE=100M
# Fri, 19 Nov 2021 11:32:58 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 19 Nov 2021 11:32:59 GMT
WORKDIR /etc/varnish
# Fri, 19 Nov 2021 11:33:00 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 19 Nov 2021 11:33:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 19 Nov 2021 11:33:01 GMT
EXPOSE 80 8443
# Fri, 19 Nov 2021 11:33:01 GMT
CMD []
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534266287933de2f8a587d9c2e3042f8a900b0ebffe6b313d30640992031e493`  
		Last Modified: Fri, 19 Nov 2021 11:35:36 GMT  
		Size: 54.4 MB (54398673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16871c8ef77ec85d93ec5c3de00e0b395ed3989ad7df1de33f9362cd661f4bb`  
		Last Modified: Fri, 19 Nov 2021 11:35:07 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:978e2e9debb586c16e6b46ff7ac1cbfc1e701dc8e71a37ff931a8bead0921584
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98448784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98bdeeb4bc344b6d4e27f4f3f079484cd5638393e08449fd5072eb43bc20209`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:32:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 04:37:17 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 04:37:17 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 04:37:19 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 04:37:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 04:37:20 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 04:37:21 GMT
CMD []
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba02b5953ea5b80ba3c0ef84066635aceff7a0a8cb96f5006de1c134d4cb91e2`  
		Last Modified: Wed, 17 Nov 2021 04:41:12 GMT  
		Size: 68.4 MB (68391561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e4c378c0c18c653a37a0d63221a0d3b8ea4e6b25988e6c70fee20c761207bf`  
		Last Modified: Wed, 17 Nov 2021 04:41:02 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6` - linux; 386

```console
$ docker pull varnish@sha256:f25bca95240699be6af700758548c536f9193baacea0b966888f3db09c93c515
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105580110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35352f71d5548760e4078ce33059d5dcb06bf29644007acd01ca4ede76822e16`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:10:10 GMT
ENV VARNISH_SIZE=100M
# Fri, 19 Nov 2021 02:15:39 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 19 Nov 2021 02:15:39 GMT
WORKDIR /etc/varnish
# Fri, 19 Nov 2021 02:15:40 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 19 Nov 2021 02:15:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 19 Nov 2021 02:15:40 GMT
EXPOSE 80 8443
# Fri, 19 Nov 2021 02:15:40 GMT
CMD []
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a3c0f8ad62670153755d6969ce97a978164c3f49fd4bd78fc717158fb43e8b`  
		Last Modified: Fri, 19 Nov 2021 02:17:05 GMT  
		Size: 73.2 MB (73198726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa39d65488c9d1db7318fb4ab937024de6b1eaf298ae2bba14594d052417bad`  
		Last Modified: Fri, 19 Nov 2021 02:16:50 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:e0b6433018298885884247c1c292bd869e42602b2f6cd74de6c6de55295d18ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103558961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2372a40b424a69707ffb97ae14efdbdec8dd2687bcbd9b8a571b5b710878da4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:04:25 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 07:08:18 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 07:08:24 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 07:08:26 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 07:08:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 07:08:33 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 07:08:38 GMT
CMD []
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9d0bd04f9bdd82973932c7ea0878410bce8db54b3dbf75aa1a8bdc94bca1c1`  
		Last Modified: Wed, 17 Nov 2021 07:37:44 GMT  
		Size: 68.3 MB (68286880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7348c6dc6d52c2df004d554143346a29441f83b45289c324aa9c08ebb8bb4a70`  
		Last Modified: Wed, 17 Nov 2021 07:37:31 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6` - linux; s390x

```console
$ docker pull varnish@sha256:14e377f6877ce74f254ed9ed95d31b7a40d16d4a62a987c4019e65d1d069301d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84737666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b27da94164283f11e04b01eaa1c5e0d71358b3249f3d1448574059b8cd14c53`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:09:56 GMT
ENV VARNISH_SIZE=100M
# Fri, 19 Nov 2021 02:11:05 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 19 Nov 2021 02:11:07 GMT
WORKDIR /etc/varnish
# Fri, 19 Nov 2021 02:11:07 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 19 Nov 2021 02:11:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 19 Nov 2021 02:11:07 GMT
EXPOSE 80 8443
# Fri, 19 Nov 2021 02:11:08 GMT
CMD []
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe324e886d9ee47afe369fd7b2c3c3e223f8213f286df5daa395bba36d378f`  
		Last Modified: Fri, 19 Nov 2021 02:12:35 GMT  
		Size: 55.1 MB (55086007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607c8fd5302cec2fa184d34ed2873b257df7dac3ba972aee15614765f9ffa43a`  
		Last Modified: Fri, 19 Nov 2021 02:12:28 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6-alpine`

```console
$ docker pull varnish@sha256:91f0f0553f56f1ddb74d05d6603a53b566a45bdbeaeef4312284e44c2b5fbf62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.6-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:452898ec4382082c43e9aad4ad2313939833ac757ed3eedf122dd4107a060862
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57989509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9452c96edc1e2f1f4f52a9471093a1f653d6266bd8a9fae81849688342d1dfcd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:25:45 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:27:11 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Mon, 29 Nov 2021 18:27:11 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:27:11 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:27:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:27:12 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:27:12 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153ae6d73742ceecdf942d8913c25adacffcf7590c180c52467774aae45fbdf8`  
		Last Modified: Mon, 29 Nov 2021 18:31:17 GMT  
		Size: 55.2 MB (55165820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47da88759d700deda407b20295e1fa1b16669b41d326a6ec602f1764725eb339`  
		Last Modified: Mon, 29 Nov 2021 18:31:09 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:aa0209cf51651473007d15a68a9e40b3ef78f01b0ca9a7b15a4465b34c44c6a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43832214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31d3ace99af9a9706f48dee76eb850e6812e89bf80a5d6a03b7f7443f000727`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:41:33 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:44:55 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:44:56 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:44:56 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:44:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:44:57 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:44:57 GMT
CMD []
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8cf867f2ac51813c0d1c016b3f20b0d9e83d4cbb126c3523cde64c96d7fcb4`  
		Last Modified: Sat, 13 Nov 2021 15:53:40 GMT  
		Size: 41.4 MB (41392891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabdbcc0379b966051181a7a466231d7e5acfefd771da959b5201467ecb927ce`  
		Last Modified: Sat, 13 Nov 2021 15:53:18 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dcad603946fbdbde3f8091aeadfec59a32593886d2a3677e06ec153999602c0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50731999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de07c78a7db786b0259191592ee3f133fe14e82e3771b98a2d89ae86740d7a04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:02:27 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 18:07:12 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 18:07:12 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 18:07:14 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:07:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 18:07:15 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 18:07:16 GMT
CMD []
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaeddc4ee611ed5f3b3af99a1d64e8a9fe9ac65234c10ae76b8f87c7408ee2c`  
		Last Modified: Fri, 12 Nov 2021 18:12:02 GMT  
		Size: 48.0 MB (48013591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb513dedceb393ae14a219dcc10e6ba648d1a3235cffeef2ba2fc580f7733e`  
		Last Modified: Fri, 12 Nov 2021 18:11:55 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6-alpine` - linux; 386

```console
$ docker pull varnish@sha256:6cd7f5496daf8d5cee94d23598c0ca332ec68a0cdc177bc9709b499ceeb281a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58198355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4b96991872090e8a8b3365cb68ba0faacaa135080273c8f4c96827c4e83a85`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:27:36 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 20:31:59 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 20:31:59 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 20:32:00 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:32:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 20:32:01 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 20:32:01 GMT
CMD []
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2418aa38a4d46c393e749f3b79218139cf03e08ee533488eef7a184ba3c4b0`  
		Last Modified: Fri, 12 Nov 2021 20:39:20 GMT  
		Size: 55.4 MB (55366703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eafccd51cc8016d5729ab976a08c451c8129732ca52bd56dad9a9d33029d19`  
		Last Modified: Fri, 12 Nov 2021 20:39:03 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:11c9146decd9c1c86e757d6bf502754bb4aaa24f4ecc70f754f98a904a167f8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47835934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174b4a7f8e1f716e198b36dcdfb63151acded0a92bd8ed4e0af888921e7b9f70`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:52:07 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:54:52 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:54:56 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:54:57 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:55:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:55:02 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:55:05 GMT
CMD []
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf90faeee149fde78cbce6fe3ba8f350dae5b3d778c56fe8cf21f7659153baf`  
		Last Modified: Sat, 13 Nov 2021 15:56:35 GMT  
		Size: 45.0 MB (45017761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d7cbba8137c7532cd04b886d9b785fcc56268da21d5cc5984a3bc67bfcacc7`  
		Last Modified: Sat, 13 Nov 2021 15:56:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:e2259beb51b142852cfcd7c82fa2289c9142678927d47a596d3ebd7cddb587ed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46372437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ece1b0b0d9a917fbd44b1e04b59716b6e8830d12011d768b6ddff4949f1951`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:22 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 22:14:23 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 22:14:27 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 22:14:27 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:14:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 22:14:28 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 22:14:28 GMT
CMD []
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1189657b7eca29d2b12d6c4c882bb5f03f6963db35b11d4b1eb816062556f71d`  
		Last Modified: Fri, 12 Nov 2021 22:16:30 GMT  
		Size: 43.8 MB (43762453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400eaf2558f0a809c40ba38f6ed62ab3abb09026784e48d056e3c07e477bfa`  
		Last Modified: Fri, 12 Nov 2021 22:16:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6.1`

```console
$ docker pull varnish@sha256:d97bb2325f93e8f11840ec5dbbecfbe0f6eafe3c65065282812dfe818490f56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.6.1` - linux; amd64

```console
$ docker pull varnish@sha256:14dc4591ca6ebc682192aeb88279148038ba1c80199db6734fd1ed3d9fe82ae1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101111708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9e2d7a898d88289a0dcaec28a767b263f436d22f9af49b303d94a3f22c9bcf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:02:38 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:26:15 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 29 Nov 2021 18:26:16 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:26:16 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:26:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:26:17 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:26:17 GMT
CMD []
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55795befb5cc32412c795a50fd294ec6bb72c993f58f3aa1e6aeb4b2632c353`  
		Last Modified: Mon, 29 Nov 2021 18:30:57 GMT  
		Size: 69.7 MB (69740739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74423f9b842a246e5b4d79beea3320392f0a3c0d50409eee98d13a45f799d6cc`  
		Last Modified: Mon, 29 Nov 2021 18:30:48 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:413095e503ec1943459aceac4700c136814ec9e17b0059fde00ac9f076071fe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80972534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f48b7cb9ce5481ed2e6b0ee90f2780f7772aa25e665040cdad90f309261a31`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 09:52:16 GMT
ENV VARNISH_SIZE=100M
# Fri, 19 Nov 2021 11:32:58 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 19 Nov 2021 11:32:59 GMT
WORKDIR /etc/varnish
# Fri, 19 Nov 2021 11:33:00 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 19 Nov 2021 11:33:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 19 Nov 2021 11:33:01 GMT
EXPOSE 80 8443
# Fri, 19 Nov 2021 11:33:01 GMT
CMD []
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534266287933de2f8a587d9c2e3042f8a900b0ebffe6b313d30640992031e493`  
		Last Modified: Fri, 19 Nov 2021 11:35:36 GMT  
		Size: 54.4 MB (54398673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16871c8ef77ec85d93ec5c3de00e0b395ed3989ad7df1de33f9362cd661f4bb`  
		Last Modified: Fri, 19 Nov 2021 11:35:07 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:978e2e9debb586c16e6b46ff7ac1cbfc1e701dc8e71a37ff931a8bead0921584
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98448784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98bdeeb4bc344b6d4e27f4f3f079484cd5638393e08449fd5072eb43bc20209`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:32:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 04:37:17 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 04:37:17 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 04:37:19 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 04:37:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 04:37:20 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 04:37:21 GMT
CMD []
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba02b5953ea5b80ba3c0ef84066635aceff7a0a8cb96f5006de1c134d4cb91e2`  
		Last Modified: Wed, 17 Nov 2021 04:41:12 GMT  
		Size: 68.4 MB (68391561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e4c378c0c18c653a37a0d63221a0d3b8ea4e6b25988e6c70fee20c761207bf`  
		Last Modified: Wed, 17 Nov 2021 04:41:02 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6.1` - linux; 386

```console
$ docker pull varnish@sha256:f25bca95240699be6af700758548c536f9193baacea0b966888f3db09c93c515
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105580110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35352f71d5548760e4078ce33059d5dcb06bf29644007acd01ca4ede76822e16`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:10:10 GMT
ENV VARNISH_SIZE=100M
# Fri, 19 Nov 2021 02:15:39 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 19 Nov 2021 02:15:39 GMT
WORKDIR /etc/varnish
# Fri, 19 Nov 2021 02:15:40 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 19 Nov 2021 02:15:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 19 Nov 2021 02:15:40 GMT
EXPOSE 80 8443
# Fri, 19 Nov 2021 02:15:40 GMT
CMD []
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a3c0f8ad62670153755d6969ce97a978164c3f49fd4bd78fc717158fb43e8b`  
		Last Modified: Fri, 19 Nov 2021 02:17:05 GMT  
		Size: 73.2 MB (73198726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa39d65488c9d1db7318fb4ab937024de6b1eaf298ae2bba14594d052417bad`  
		Last Modified: Fri, 19 Nov 2021 02:16:50 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:e0b6433018298885884247c1c292bd869e42602b2f6cd74de6c6de55295d18ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103558961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2372a40b424a69707ffb97ae14efdbdec8dd2687bcbd9b8a571b5b710878da4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:04:25 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 07:08:18 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 07:08:24 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 07:08:26 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 07:08:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 07:08:33 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 07:08:38 GMT
CMD []
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9d0bd04f9bdd82973932c7ea0878410bce8db54b3dbf75aa1a8bdc94bca1c1`  
		Last Modified: Wed, 17 Nov 2021 07:37:44 GMT  
		Size: 68.3 MB (68286880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7348c6dc6d52c2df004d554143346a29441f83b45289c324aa9c08ebb8bb4a70`  
		Last Modified: Wed, 17 Nov 2021 07:37:31 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6.1` - linux; s390x

```console
$ docker pull varnish@sha256:14e377f6877ce74f254ed9ed95d31b7a40d16d4a62a987c4019e65d1d069301d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84737666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b27da94164283f11e04b01eaa1c5e0d71358b3249f3d1448574059b8cd14c53`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:09:56 GMT
ENV VARNISH_SIZE=100M
# Fri, 19 Nov 2021 02:11:05 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 19 Nov 2021 02:11:07 GMT
WORKDIR /etc/varnish
# Fri, 19 Nov 2021 02:11:07 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 19 Nov 2021 02:11:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 19 Nov 2021 02:11:07 GMT
EXPOSE 80 8443
# Fri, 19 Nov 2021 02:11:08 GMT
CMD []
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe324e886d9ee47afe369fd7b2c3c3e223f8213f286df5daa395bba36d378f`  
		Last Modified: Fri, 19 Nov 2021 02:12:35 GMT  
		Size: 55.1 MB (55086007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607c8fd5302cec2fa184d34ed2873b257df7dac3ba972aee15614765f9ffa43a`  
		Last Modified: Fri, 19 Nov 2021 02:12:28 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6.1-alpine`

```console
$ docker pull varnish@sha256:91f0f0553f56f1ddb74d05d6603a53b566a45bdbeaeef4312284e44c2b5fbf62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.6.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:452898ec4382082c43e9aad4ad2313939833ac757ed3eedf122dd4107a060862
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57989509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9452c96edc1e2f1f4f52a9471093a1f653d6266bd8a9fae81849688342d1dfcd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:25:45 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:27:11 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Mon, 29 Nov 2021 18:27:11 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:27:11 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:27:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:27:12 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:27:12 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153ae6d73742ceecdf942d8913c25adacffcf7590c180c52467774aae45fbdf8`  
		Last Modified: Mon, 29 Nov 2021 18:31:17 GMT  
		Size: 55.2 MB (55165820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47da88759d700deda407b20295e1fa1b16669b41d326a6ec602f1764725eb339`  
		Last Modified: Mon, 29 Nov 2021 18:31:09 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:aa0209cf51651473007d15a68a9e40b3ef78f01b0ca9a7b15a4465b34c44c6a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43832214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31d3ace99af9a9706f48dee76eb850e6812e89bf80a5d6a03b7f7443f000727`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:41:33 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:44:55 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:44:56 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:44:56 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:44:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:44:57 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:44:57 GMT
CMD []
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8cf867f2ac51813c0d1c016b3f20b0d9e83d4cbb126c3523cde64c96d7fcb4`  
		Last Modified: Sat, 13 Nov 2021 15:53:40 GMT  
		Size: 41.4 MB (41392891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabdbcc0379b966051181a7a466231d7e5acfefd771da959b5201467ecb927ce`  
		Last Modified: Sat, 13 Nov 2021 15:53:18 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dcad603946fbdbde3f8091aeadfec59a32593886d2a3677e06ec153999602c0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50731999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de07c78a7db786b0259191592ee3f133fe14e82e3771b98a2d89ae86740d7a04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:02:27 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 18:07:12 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 18:07:12 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 18:07:14 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:07:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 18:07:15 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 18:07:16 GMT
CMD []
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaeddc4ee611ed5f3b3af99a1d64e8a9fe9ac65234c10ae76b8f87c7408ee2c`  
		Last Modified: Fri, 12 Nov 2021 18:12:02 GMT  
		Size: 48.0 MB (48013591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb513dedceb393ae14a219dcc10e6ba648d1a3235cffeef2ba2fc580f7733e`  
		Last Modified: Fri, 12 Nov 2021 18:11:55 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:6cd7f5496daf8d5cee94d23598c0ca332ec68a0cdc177bc9709b499ceeb281a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58198355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4b96991872090e8a8b3365cb68ba0faacaa135080273c8f4c96827c4e83a85`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:27:36 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 20:31:59 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 20:31:59 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 20:32:00 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:32:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 20:32:01 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 20:32:01 GMT
CMD []
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2418aa38a4d46c393e749f3b79218139cf03e08ee533488eef7a184ba3c4b0`  
		Last Modified: Fri, 12 Nov 2021 20:39:20 GMT  
		Size: 55.4 MB (55366703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eafccd51cc8016d5729ab976a08c451c8129732ca52bd56dad9a9d33029d19`  
		Last Modified: Fri, 12 Nov 2021 20:39:03 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:11c9146decd9c1c86e757d6bf502754bb4aaa24f4ecc70f754f98a904a167f8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47835934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174b4a7f8e1f716e198b36dcdfb63151acded0a92bd8ed4e0af888921e7b9f70`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:52:07 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:54:52 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:54:56 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:54:57 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:55:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:55:02 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:55:05 GMT
CMD []
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf90faeee149fde78cbce6fe3ba8f350dae5b3d778c56fe8cf21f7659153baf`  
		Last Modified: Sat, 13 Nov 2021 15:56:35 GMT  
		Size: 45.0 MB (45017761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d7cbba8137c7532cd04b886d9b785fcc56268da21d5cc5984a3bc67bfcacc7`  
		Last Modified: Sat, 13 Nov 2021 15:56:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.6.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:e2259beb51b142852cfcd7c82fa2289c9142678927d47a596d3ebd7cddb587ed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46372437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ece1b0b0d9a917fbd44b1e04b59716b6e8830d12011d768b6ddff4949f1951`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:22 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 22:14:23 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 22:14:27 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 22:14:27 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:14:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 22:14:28 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 22:14:28 GMT
CMD []
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1189657b7eca29d2b12d6c4c882bb5f03f6963db35b11d4b1eb816062556f71d`  
		Last Modified: Fri, 12 Nov 2021 22:16:30 GMT  
		Size: 43.8 MB (43762453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400eaf2558f0a809c40ba38f6ed62ab3abb09026784e48d056e3c07e477bfa`  
		Last Modified: Fri, 12 Nov 2021 22:16:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.0`

```console
$ docker pull varnish@sha256:275f630c142128fff6208ce00a2596d21d153cbe23ec8e7725fea4a14bac8fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.0` - linux; amd64

```console
$ docker pull varnish@sha256:d3855cf0414ce764e06e30dd3ffda862b7aa3d68f86d98da40a9e7fc1587c7c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101190955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3658dee045ef52cd3218f3cc88c4e4a9cf4f9105d486b7aba50a70160087c42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:02:38 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:22:36 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.1.tgz -o $tmpdir/orig.tgz;     echo "7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 29 Nov 2021 18:22:37 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:22:37 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:22:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:22:37 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:22:37 GMT
CMD []
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322bd05dea04ce119109555b9a65a488419a6aa963fb6d47943d7e34b78ba8b2`  
		Last Modified: Mon, 29 Nov 2021 18:30:11 GMT  
		Size: 69.8 MB (69820212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e3c589fc5a0354e3bdf0ff5d10e4a1f5e03a7ff4f2d790058ca309b1b1b7e9`  
		Last Modified: Mon, 29 Nov 2021 18:30:02 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c240e795e9d62cb28f000d79d4217892527ccb7ba16c15956f46f84eeaa6a041
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81217264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa82400ddb1489e132ea9fc08044a8414e5f6497bdd5d85f070d7213dd5d8be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 09:52:16 GMT
ENV VARNISH_SIZE=100M
# Thu, 18 Nov 2021 09:57:57 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 18 Nov 2021 09:57:58 GMT
WORKDIR /etc/varnish
# Thu, 18 Nov 2021 09:57:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 18 Nov 2021 09:57:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 18 Nov 2021 09:57:59 GMT
EXPOSE 80 8443
# Thu, 18 Nov 2021 09:58:00 GMT
CMD []
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995a81b2cb29588b95194d051d0db4ad26537aaf524bed3daa994739dbb67e27`  
		Last Modified: Thu, 18 Nov 2021 10:06:50 GMT  
		Size: 54.6 MB (54643631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0ad718cf28c5982b42621ef4bf65053b627878d4c49c7dde6b3f1dcfbe9156`  
		Last Modified: Thu, 18 Nov 2021 10:06:21 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:331e3ee5311aa4b31e5f8faacca07b84bd9173bfe5ba1e19e47148f862f09b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98702970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a951c912ec6ea48924d63ee40547975645660c14694ee1af097a24ffce7b149`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:32:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 04:34:37 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 04:34:38 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 04:34:39 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 04:34:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 04:34:40 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 04:34:41 GMT
CMD []
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eb9388ba1f805feffd8319d25466baeadd9f2d695f2aabc1b8444fc79cf250`  
		Last Modified: Wed, 17 Nov 2021 04:40:43 GMT  
		Size: 68.6 MB (68645975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e54176b0a037e66e61c824ba75ab82b47ba1e3e0fb2778c6a4e29c166e1a9a5`  
		Last Modified: Wed, 17 Nov 2021 04:40:33 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0` - linux; 386

```console
$ docker pull varnish@sha256:50233d97f281820ca5abc37f58836a60ce0373326b786b9056f8171ce2d3f0f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105802766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fc2c2a2308e428482a33014c6cd52b1e77773c168972e9636c857d2eacf078`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:10:10 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 03:13:22 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 03:13:23 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 03:13:23 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 03:13:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 03:13:24 GMT
CMD []
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6da7e8bf779c7a01eff42003ce0234602d48047066bdae20757149f130940e`  
		Last Modified: Wed, 17 Nov 2021 03:18:12 GMT  
		Size: 73.4 MB (73421610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737ddd62e39b33ec70b8bda30309091c785af357bd9dbab9e8b71408188bfc2c`  
		Last Modified: Wed, 17 Nov 2021 03:17:58 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:9c1ea9b3990ca7a9106f0a8ec8b5cc38f4de5161912e2c2481a88b7459ba14f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103805146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ea3420500395a52f3cbbaa26ea64adacb99d5dce8f2e24baa6d1583465061f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:04:25 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 06:33:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 06:34:03 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 06:34:07 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 06:34:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 06:34:23 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 06:34:29 GMT
CMD []
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede74025f453eb239899d64b9466f119dc2f664e82b1529db59b5385dca93f18`  
		Last Modified: Wed, 17 Nov 2021 07:37:12 GMT  
		Size: 68.5 MB (68533289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab465f900cffa890ba81f5102d4613ced3e455e7c2ee38240330afd97d791da1`  
		Last Modified: Wed, 17 Nov 2021 07:36:59 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0` - linux; s390x

```console
$ docker pull varnish@sha256:e522646171effb2ec075821c7e8a8b1c60028f2d3203ed41d6b3da98e4e91dec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85001090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5981679e033a9ac77cd2b7a70bfbd08ca4c650d4dff4b879461ded143ea40d04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:09:56 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 12:11:39 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 12:11:41 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 12:11:41 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 12:11:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 12:11:42 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 12:11:42 GMT
CMD []
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e14d21e5759658aedc62cd484439b3dc09cbdc979419679d402bd0a9409fbd`  
		Last Modified: Wed, 17 Nov 2021 12:13:55 GMT  
		Size: 55.3 MB (55349657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653d8908e660daa2a0615175ca8590b144cdd5aa6ee2652e83e6429ffee8cc47`  
		Last Modified: Wed, 17 Nov 2021 12:13:47 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.0-alpine`

```console
$ docker pull varnish@sha256:992c4786eeaa7c7d153d473fa819d9eb665c94790fc4ab000cbe46f774c16a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:e6f6804aecc2fb6b091c54021c1773b77968d798293d41ab3ee46f5c00a58bb1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58362658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7e9599575e47151d14b79975fd45baf80559233e36487f2ce8bbe0a941ce68`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:25:45 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:23:42 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Mon, 29 Nov 2021 18:23:42 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:23:42 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:23:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:23:43 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:23:43 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf619492e89f6485a3ba5e7cb6807f6f35a59e5715d4bffcb692cfecddeefbd8`  
		Last Modified: Mon, 29 Nov 2021 18:30:34 GMT  
		Size: 55.5 MB (55539197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a667c3f673f5f288f2ff0a45cd4743280d929515d6979127e0cb9f843854d03`  
		Last Modified: Mon, 29 Nov 2021 18:30:26 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:07a11ace7bd317e07641faf0290a9c424f2807c71c771ba4112352ed01edb825
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44182663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5d3f39fab82aae82e0040de663009d9179c71d25aaa0f9f4f6c17dfd46917`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:41:33 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:43:01 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:43:02 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:43:03 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:43:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:43:03 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:43:04 GMT
CMD []
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6b7000342f95d46e5b48cfb7808d094fed8f3d82d54dbcae041ff5797e12e`  
		Last Modified: Sat, 13 Nov 2021 15:52:55 GMT  
		Size: 41.7 MB (41743567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9935ad4b54275bc2d461752cccef1d67e3625f43d41fca9f5f7fee10b0c581`  
		Last Modified: Sat, 13 Nov 2021 15:52:33 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:be906da2df7baeb35e33f21bb8b8569ca0cd3dcbf82f8325d387d409591e3341
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51108617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfad9e9cf640629bd0b7fe5970fbd652fb0450e6093adc58f4ae8781952b15c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:02:27 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 18:03:26 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 18:03:26 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 18:03:28 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:03:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 18:03:29 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 18:03:30 GMT
CMD []
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3156901f263be485231564efa49a95ae550f773936fcb146bc72ea32290ce733`  
		Last Modified: Fri, 12 Nov 2021 18:11:15 GMT  
		Size: 48.4 MB (48390438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5847cbe7d8162260bce419a5cb61ea09c1c93dc5e2bcd2b82d7e471fe269b907`  
		Last Modified: Fri, 12 Nov 2021 18:11:08 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:5197a57c34b3bd99ff5f8978737afc8422cd2c3f4c4b2622fc512c1bea56687c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58575907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b4da6c280c940a6fbe5cd93c6db63f23ba47e4de7ae74747c09ff56e2dd6af`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:27:36 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 20:29:32 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 20:29:33 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 20:29:33 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:29:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 20:29:34 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 20:29:35 GMT
CMD []
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2114eb284e1895354c615e8d675c2f51ea4b035086fe3990c5f7984bd37a0d`  
		Last Modified: Fri, 12 Nov 2021 20:38:38 GMT  
		Size: 55.7 MB (55744480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595cf1ed60723c431100d3228748183b34d9fec17114ef1d41f2e146a0172d58`  
		Last Modified: Fri, 12 Nov 2021 20:38:22 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:d01f07394fd2866aa545843ec1ff1e642d012d7b4c7cd9608e9dd481107b792e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48224608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2088057097d9716eee0d9dd9a041aa3ed9060a7a69fef1f35cf0ac516e0e8f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:52:07 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:53:18 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:53:23 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:53:23 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:53:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:53:27 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:53:32 GMT
CMD []
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f0b2c9903ecdaa15af2cabffb8e77f729da6dfd894a82938d64d8b6d92d630`  
		Last Modified: Sat, 13 Nov 2021 15:56:08 GMT  
		Size: 45.4 MB (45406662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53a44be231651b43f32bc477da875668dce263febec9ea0ac7dd322240fd334`  
		Last Modified: Sat, 13 Nov 2021 15:55:59 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ee47cf4c694d03327082b6ee67238206cd2586fd0122504982e334112691d7b5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46691858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf47f559ece084de3bd316f80ae674f00135b5b29d2922a5288c000964c8944`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:22 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 22:10:58 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 22:10:59 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 22:11:00 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:11:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 22:11:00 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 22:11:00 GMT
CMD []
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a59e55e723ec8fecb8ce8cac9c1ae3fd531846ef446d9f964d54ce8a381edc`  
		Last Modified: Fri, 12 Nov 2021 22:15:55 GMT  
		Size: 44.1 MB (44082103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483f8807a2f1038904772cff0766c6251ef9ed695640f95fa1a9807fed849c01`  
		Last Modified: Fri, 12 Nov 2021 22:15:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.0.1`

```console
$ docker pull varnish@sha256:8f478c1aeff16161ef91ec427ce361e6e1cd3aefaca4f1d08c91754f93492d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.0.1` - linux; amd64

```console
$ docker pull varnish@sha256:d3855cf0414ce764e06e30dd3ffda862b7aa3d68f86d98da40a9e7fc1587c7c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101190955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3658dee045ef52cd3218f3cc88c4e4a9cf4f9105d486b7aba50a70160087c42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:02:38 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:22:36 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.1.tgz -o $tmpdir/orig.tgz;     echo "7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 29 Nov 2021 18:22:37 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:22:37 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:22:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:22:37 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:22:37 GMT
CMD []
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322bd05dea04ce119109555b9a65a488419a6aa963fb6d47943d7e34b78ba8b2`  
		Last Modified: Mon, 29 Nov 2021 18:30:11 GMT  
		Size: 69.8 MB (69820212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e3c589fc5a0354e3bdf0ff5d10e4a1f5e03a7ff4f2d790058ca309b1b1b7e9`  
		Last Modified: Mon, 29 Nov 2021 18:30:02 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:47b0299239bb3de6bab6081403776f14cbf503316c1c080bc417a4b4cf8ddcd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77812702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a29f3140eb01edff353258cdb556c555fde9b0d3b59fcfc91b21a90c8451e22`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 09:52:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Nov 2021 19:10:31 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.1.tgz -o $tmpdir/orig.tgz;     echo "7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";     chown varnish /var/lib/varnish
# Tue, 23 Nov 2021 19:10:32 GMT
WORKDIR /etc/varnish
# Tue, 23 Nov 2021 19:10:33 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 23 Nov 2021 19:10:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Nov 2021 19:10:34 GMT
USER varnish
# Tue, 23 Nov 2021 19:10:34 GMT
EXPOSE 80 8443
# Tue, 23 Nov 2021 19:10:34 GMT
CMD []
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae63f21c0227467ac900beadd707c59d7b8fd52888096866c35adbb9463397d3`  
		Last Modified: Tue, 23 Nov 2021 19:23:15 GMT  
		Size: 51.2 MB (51239068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28201dcec8350036f4195ef5f36393a9084093043b912e3967a6e440fa9a69a8`  
		Last Modified: Tue, 23 Nov 2021 19:22:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:51aff26cb39a2f14fce2e947c23faa09d25dd0a913916db912b7a499e26fa2ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95302102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e131f007cc132b8f6dd08e780522dd2e60731dbe2e0f823ed11e14f40cac89b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:32:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Nov 2021 18:45:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.1.tgz -o $tmpdir/orig.tgz;     echo "7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";     chown varnish /var/lib/varnish
# Tue, 23 Nov 2021 18:45:49 GMT
WORKDIR /etc/varnish
# Tue, 23 Nov 2021 18:45:50 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 23 Nov 2021 18:45:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Nov 2021 18:45:51 GMT
USER varnish
# Tue, 23 Nov 2021 18:45:52 GMT
EXPOSE 80 8443
# Tue, 23 Nov 2021 18:45:53 GMT
CMD []
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578fcb2ffb3a65568d2158fff866790a57bef5ff9fe4d0adbc8638903200d063`  
		Last Modified: Tue, 23 Nov 2021 18:53:53 GMT  
		Size: 65.2 MB (65245109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2e44ba19c44d8707ddcfa7453b71f4bbf425fd6598d105594e436984544e0d`  
		Last Modified: Tue, 23 Nov 2021 18:53:43 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:62015f62c67f63ec23add010e41f2ac9dfd880362c44a690dd974ce17e5e3751
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100359492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cb11f686ef357f33a8e37968cc67ae542dffe603cf9aff29394368a198052c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:04:25 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Nov 2021 19:23:45 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.1.tgz -o $tmpdir/orig.tgz;     echo "7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";     chown varnish /var/lib/varnish
# Tue, 23 Nov 2021 19:23:53 GMT
WORKDIR /etc/varnish
# Tue, 23 Nov 2021 19:23:56 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 23 Nov 2021 19:23:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Nov 2021 19:24:01 GMT
USER varnish
# Tue, 23 Nov 2021 19:24:05 GMT
EXPOSE 80 8443
# Tue, 23 Nov 2021 19:24:08 GMT
CMD []
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d18b72ed51762923dec234a3e6d8a5cab5a3021ae2c28a3554deb133f6e21a`  
		Last Modified: Tue, 23 Nov 2021 20:12:14 GMT  
		Size: 65.1 MB (65087635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af30865388f39d784806088616002d8919fb85e113af44fb1e91c8c5c916821`  
		Last Modified: Tue, 23 Nov 2021 20:12:01 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.1` - linux; s390x

```console
$ docker pull varnish@sha256:a3c56f087d0388cf65564d909213dce9beb41bb76957ef33e200e114cfdec496
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81633627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f030b8a4929d9f6b3c7ddec396a27c9882ba5fd55bffb52d02838837b50f773e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:09:56 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Nov 2021 18:47:33 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.1.tgz -o $tmpdir/orig.tgz;     echo "7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";     chown varnish /var/lib/varnish
# Tue, 23 Nov 2021 18:47:35 GMT
WORKDIR /etc/varnish
# Tue, 23 Nov 2021 18:47:35 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 23 Nov 2021 18:47:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Nov 2021 18:47:35 GMT
USER varnish
# Tue, 23 Nov 2021 18:47:35 GMT
EXPOSE 80 8443
# Tue, 23 Nov 2021 18:47:35 GMT
CMD []
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1856848ea6559ab3eee68b844d86e89b75e816219e79719ab420902c863da945`  
		Last Modified: Tue, 23 Nov 2021 18:54:08 GMT  
		Size: 52.0 MB (51982194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebb5c6d1e9db1bb11962fac5aa107d6b0984baa8dfa3186eea6afedfa98c1fd`  
		Last Modified: Tue, 23 Nov 2021 18:54:01 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.0.1-alpine`

```console
$ docker pull varnish@sha256:9513f1b1cd2e4b3db289be44f9c10cff884ab3b7a7cde6500a7e9e7902a838f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.0.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:e6f6804aecc2fb6b091c54021c1773b77968d798293d41ab3ee46f5c00a58bb1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58362658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7e9599575e47151d14b79975fd45baf80559233e36487f2ce8bbe0a941ce68`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:25:45 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:23:42 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Mon, 29 Nov 2021 18:23:42 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:23:42 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:23:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:23:43 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:23:43 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf619492e89f6485a3ba5e7cb6807f6f35a59e5715d4bffcb692cfecddeefbd8`  
		Last Modified: Mon, 29 Nov 2021 18:30:34 GMT  
		Size: 55.5 MB (55539197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a667c3f673f5f288f2ff0a45cd4743280d929515d6979127e0cb9f843854d03`  
		Last Modified: Mon, 29 Nov 2021 18:30:26 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:f92f1bece504af1f0093449fadb1d28a0767c6f85ce8c91f540cd544d16bccf2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44177057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5494ad27b26f4820a59717caf166e72c8577a40bc95fa40f336c0ec0154ec191`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:41:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Nov 2021 19:12:23 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;     chown varnish /var/lib/varnish
# Tue, 23 Nov 2021 19:12:23 GMT
WORKDIR /etc/varnish
# Tue, 23 Nov 2021 19:12:24 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 23 Nov 2021 19:12:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Nov 2021 19:12:25 GMT
USER varnish
# Tue, 23 Nov 2021 19:12:25 GMT
EXPOSE 80 8443
# Tue, 23 Nov 2021 19:12:26 GMT
CMD []
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168a98bbefabd5e361ec90253b9467371b2610302f0ce9d8177ebcababdba1a7`  
		Last Modified: Tue, 23 Nov 2021 19:23:56 GMT  
		Size: 41.7 MB (41737960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f53c5d7a015c9af053287535ac210bd9c74f787646169c50d5bca058b730ba`  
		Last Modified: Tue, 23 Nov 2021 19:23:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b3ec9620791fcf441a8f754a3ae153982688a0c358ecbcb541905e2c24d760a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51095518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26159e0db97873e3a5a8a98aaf7c1cf40c468e6a79b58b9f374c740e400c0b6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:02:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Nov 2021 18:46:59 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;     chown varnish /var/lib/varnish
# Tue, 23 Nov 2021 18:46:59 GMT
WORKDIR /etc/varnish
# Tue, 23 Nov 2021 18:47:01 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 23 Nov 2021 18:47:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Nov 2021 18:47:02 GMT
USER varnish
# Tue, 23 Nov 2021 18:47:03 GMT
EXPOSE 80 8443
# Tue, 23 Nov 2021 18:47:04 GMT
CMD []
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1818711e82171f58532be9e36ece4bea66ada8827cf9c5ebd8f1b7ea37e7c7c8`  
		Last Modified: Tue, 23 Nov 2021 18:54:17 GMT  
		Size: 48.4 MB (48377338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61a4444a0bd5c82c31470ed5b05658aae067d486a26c47ba35ea28ccaa50d9`  
		Last Modified: Tue, 23 Nov 2021 18:54:09 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:7e707761beaed2fb05c8056028f69eaebc2a2fa88c2ed739999372cc4757d768
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58572045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dfa4bd8e34ecd915f99227bd2dbf832a2378fc76bf526cf79bc627ba6c5a97`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:27:36 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Nov 2021 18:42:31 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;     chown varnish /var/lib/varnish
# Tue, 23 Nov 2021 18:42:32 GMT
WORKDIR /etc/varnish
# Tue, 23 Nov 2021 18:42:32 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 23 Nov 2021 18:42:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Nov 2021 18:42:32 GMT
USER varnish
# Tue, 23 Nov 2021 18:42:32 GMT
EXPOSE 80 8443
# Tue, 23 Nov 2021 18:42:33 GMT
CMD []
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c4383f662e95079222ca9eaaae58b7810e2800ff07ae1741ee630c0e77a4c8`  
		Last Modified: Tue, 23 Nov 2021 18:47:45 GMT  
		Size: 55.7 MB (55740616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238fb00b824da3ba7d7b183776ef986cafdad5a53a64857b7c8820413f8d9b3f`  
		Last Modified: Tue, 23 Nov 2021 18:47:35 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:82158bd40b9d5e4bc2c78be680082978f6c8d9561bc66d91b61704784025b8f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48217443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d83fcb273a473c14857b2126edaaa4803dd101a1eef640d4404359a744c5dd7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:52:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Nov 2021 19:25:37 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;     chown varnish /var/lib/varnish
# Tue, 23 Nov 2021 19:25:40 GMT
WORKDIR /etc/varnish
# Tue, 23 Nov 2021 19:25:43 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 23 Nov 2021 19:25:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Nov 2021 19:25:48 GMT
USER varnish
# Tue, 23 Nov 2021 19:25:52 GMT
EXPOSE 80 8443
# Tue, 23 Nov 2021 19:25:54 GMT
CMD []
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e264a0d3f91805f5cc7410cb1d330a98486598c9a7fe23b65d6c779465ec3f0`  
		Last Modified: Tue, 23 Nov 2021 20:12:39 GMT  
		Size: 45.4 MB (45399496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a36b52ccb7fa4f0804b44fffb700d4487814ba5baa1e90c3de9127f0701185`  
		Last Modified: Tue, 23 Nov 2021 20:12:30 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.0.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7332cb5e538e4ce7b2cbea1f5df22d4cfb5f25ae86c3a372ce2cfdad56358fe1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46684103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d336021b72dc6a8230d1ced495f049cc1cd444e4388e7f4c8f030f4a5c082d1a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:22 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Nov 2021 18:48:19 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;     chown varnish /var/lib/varnish
# Tue, 23 Nov 2021 18:48:20 GMT
WORKDIR /etc/varnish
# Tue, 23 Nov 2021 18:48:20 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 23 Nov 2021 18:48:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Nov 2021 18:48:20 GMT
USER varnish
# Tue, 23 Nov 2021 18:48:21 GMT
EXPOSE 80 8443
# Tue, 23 Nov 2021 18:48:21 GMT
CMD []
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150943b9444243ba5bcc08c008ddc0e099f980cc43f0e4221324bb47e961ea34`  
		Last Modified: Tue, 23 Nov 2021 18:54:25 GMT  
		Size: 44.1 MB (44074346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303a433a4cc94594e14447d74042ee6129d8c5864b4d25d42d1e98ff0372f845`  
		Last Modified: Tue, 23 Nov 2021 18:54:19 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:alpine`

```console
$ docker pull varnish@sha256:992c4786eeaa7c7d153d473fa819d9eb665c94790fc4ab000cbe46f774c16a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:e6f6804aecc2fb6b091c54021c1773b77968d798293d41ab3ee46f5c00a58bb1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58362658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7e9599575e47151d14b79975fd45baf80559233e36487f2ce8bbe0a941ce68`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:25:45 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:23:42 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Mon, 29 Nov 2021 18:23:42 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:23:42 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:23:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:23:43 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:23:43 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf619492e89f6485a3ba5e7cb6807f6f35a59e5715d4bffcb692cfecddeefbd8`  
		Last Modified: Mon, 29 Nov 2021 18:30:34 GMT  
		Size: 55.5 MB (55539197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a667c3f673f5f288f2ff0a45cd4743280d929515d6979127e0cb9f843854d03`  
		Last Modified: Mon, 29 Nov 2021 18:30:26 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:07a11ace7bd317e07641faf0290a9c424f2807c71c771ba4112352ed01edb825
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44182663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5d3f39fab82aae82e0040de663009d9179c71d25aaa0f9f4f6c17dfd46917`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:41:33 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:43:01 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:43:02 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:43:03 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:43:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:43:03 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:43:04 GMT
CMD []
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6b7000342f95d46e5b48cfb7808d094fed8f3d82d54dbcae041ff5797e12e`  
		Last Modified: Sat, 13 Nov 2021 15:52:55 GMT  
		Size: 41.7 MB (41743567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9935ad4b54275bc2d461752cccef1d67e3625f43d41fca9f5f7fee10b0c581`  
		Last Modified: Sat, 13 Nov 2021 15:52:33 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:be906da2df7baeb35e33f21bb8b8569ca0cd3dcbf82f8325d387d409591e3341
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51108617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfad9e9cf640629bd0b7fe5970fbd652fb0450e6093adc58f4ae8781952b15c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:02:27 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 18:03:26 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 18:03:26 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 18:03:28 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:03:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 18:03:29 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 18:03:30 GMT
CMD []
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3156901f263be485231564efa49a95ae550f773936fcb146bc72ea32290ce733`  
		Last Modified: Fri, 12 Nov 2021 18:11:15 GMT  
		Size: 48.4 MB (48390438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5847cbe7d8162260bce419a5cb61ea09c1c93dc5e2bcd2b82d7e471fe269b907`  
		Last Modified: Fri, 12 Nov 2021 18:11:08 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:5197a57c34b3bd99ff5f8978737afc8422cd2c3f4c4b2622fc512c1bea56687c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58575907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b4da6c280c940a6fbe5cd93c6db63f23ba47e4de7ae74747c09ff56e2dd6af`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:27:36 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 20:29:32 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 20:29:33 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 20:29:33 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:29:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 20:29:34 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 20:29:35 GMT
CMD []
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2114eb284e1895354c615e8d675c2f51ea4b035086fe3990c5f7984bd37a0d`  
		Last Modified: Fri, 12 Nov 2021 20:38:38 GMT  
		Size: 55.7 MB (55744480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595cf1ed60723c431100d3228748183b34d9fec17114ef1d41f2e146a0172d58`  
		Last Modified: Fri, 12 Nov 2021 20:38:22 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:d01f07394fd2866aa545843ec1ff1e642d012d7b4c7cd9608e9dd481107b792e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48224608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2088057097d9716eee0d9dd9a041aa3ed9060a7a69fef1f35cf0ac516e0e8f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:52:07 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:53:18 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:53:23 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:53:23 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:53:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:53:27 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:53:32 GMT
CMD []
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f0b2c9903ecdaa15af2cabffb8e77f729da6dfd894a82938d64d8b6d92d630`  
		Last Modified: Sat, 13 Nov 2021 15:56:08 GMT  
		Size: 45.4 MB (45406662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53a44be231651b43f32bc477da875668dce263febec9ea0ac7dd322240fd334`  
		Last Modified: Sat, 13 Nov 2021 15:55:59 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ee47cf4c694d03327082b6ee67238206cd2586fd0122504982e334112691d7b5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46691858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf47f559ece084de3bd316f80ae674f00135b5b29d2922a5288c000964c8944`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:22 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 22:10:58 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 22:10:59 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 22:11:00 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:11:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 22:11:00 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 22:11:00 GMT
CMD []
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a59e55e723ec8fecb8ce8cac9c1ae3fd531846ef446d9f964d54ce8a381edc`  
		Last Modified: Fri, 12 Nov 2021 22:15:55 GMT  
		Size: 44.1 MB (44082103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483f8807a2f1038904772cff0766c6251ef9ed695640f95fa1a9807fed849c01`  
		Last Modified: Fri, 12 Nov 2021 22:15:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:275f630c142128fff6208ce00a2596d21d153cbe23ec8e7725fea4a14bac8fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:d3855cf0414ce764e06e30dd3ffda862b7aa3d68f86d98da40a9e7fc1587c7c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101190955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3658dee045ef52cd3218f3cc88c4e4a9cf4f9105d486b7aba50a70160087c42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:02:38 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:22:36 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.1.tgz -o $tmpdir/orig.tgz;     echo "7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 29 Nov 2021 18:22:37 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:22:37 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:22:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:22:37 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:22:37 GMT
CMD []
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322bd05dea04ce119109555b9a65a488419a6aa963fb6d47943d7e34b78ba8b2`  
		Last Modified: Mon, 29 Nov 2021 18:30:11 GMT  
		Size: 69.8 MB (69820212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e3c589fc5a0354e3bdf0ff5d10e4a1f5e03a7ff4f2d790058ca309b1b1b7e9`  
		Last Modified: Mon, 29 Nov 2021 18:30:02 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c240e795e9d62cb28f000d79d4217892527ccb7ba16c15956f46f84eeaa6a041
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81217264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa82400ddb1489e132ea9fc08044a8414e5f6497bdd5d85f070d7213dd5d8be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 09:52:16 GMT
ENV VARNISH_SIZE=100M
# Thu, 18 Nov 2021 09:57:57 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 18 Nov 2021 09:57:58 GMT
WORKDIR /etc/varnish
# Thu, 18 Nov 2021 09:57:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 18 Nov 2021 09:57:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 18 Nov 2021 09:57:59 GMT
EXPOSE 80 8443
# Thu, 18 Nov 2021 09:58:00 GMT
CMD []
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995a81b2cb29588b95194d051d0db4ad26537aaf524bed3daa994739dbb67e27`  
		Last Modified: Thu, 18 Nov 2021 10:06:50 GMT  
		Size: 54.6 MB (54643631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0ad718cf28c5982b42621ef4bf65053b627878d4c49c7dde6b3f1dcfbe9156`  
		Last Modified: Thu, 18 Nov 2021 10:06:21 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:331e3ee5311aa4b31e5f8faacca07b84bd9173bfe5ba1e19e47148f862f09b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98702970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a951c912ec6ea48924d63ee40547975645660c14694ee1af097a24ffce7b149`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:32:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 04:34:37 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 04:34:38 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 04:34:39 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 04:34:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 04:34:40 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 04:34:41 GMT
CMD []
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eb9388ba1f805feffd8319d25466baeadd9f2d695f2aabc1b8444fc79cf250`  
		Last Modified: Wed, 17 Nov 2021 04:40:43 GMT  
		Size: 68.6 MB (68645975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e54176b0a037e66e61c824ba75ab82b47ba1e3e0fb2778c6a4e29c166e1a9a5`  
		Last Modified: Wed, 17 Nov 2021 04:40:33 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:50233d97f281820ca5abc37f58836a60ce0373326b786b9056f8171ce2d3f0f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105802766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fc2c2a2308e428482a33014c6cd52b1e77773c168972e9636c857d2eacf078`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:10:10 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 03:13:22 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 03:13:23 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 03:13:23 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 03:13:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 03:13:24 GMT
CMD []
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6da7e8bf779c7a01eff42003ce0234602d48047066bdae20757149f130940e`  
		Last Modified: Wed, 17 Nov 2021 03:18:12 GMT  
		Size: 73.4 MB (73421610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737ddd62e39b33ec70b8bda30309091c785af357bd9dbab9e8b71408188bfc2c`  
		Last Modified: Wed, 17 Nov 2021 03:17:58 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:9c1ea9b3990ca7a9106f0a8ec8b5cc38f4de5161912e2c2481a88b7459ba14f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103805146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ea3420500395a52f3cbbaa26ea64adacb99d5dce8f2e24baa6d1583465061f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:04:25 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 06:33:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 06:34:03 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 06:34:07 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 06:34:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 06:34:23 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 06:34:29 GMT
CMD []
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede74025f453eb239899d64b9466f119dc2f664e82b1529db59b5385dca93f18`  
		Last Modified: Wed, 17 Nov 2021 07:37:12 GMT  
		Size: 68.5 MB (68533289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab465f900cffa890ba81f5102d4613ced3e455e7c2ee38240330afd97d791da1`  
		Last Modified: Wed, 17 Nov 2021 07:36:59 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:e522646171effb2ec075821c7e8a8b1c60028f2d3203ed41d6b3da98e4e91dec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85001090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5981679e033a9ac77cd2b7a70bfbd08ca4c650d4dff4b879461ded143ea40d04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:09:56 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 12:11:39 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 12:11:41 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 12:11:41 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 12:11:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 12:11:42 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 12:11:42 GMT
CMD []
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e14d21e5759658aedc62cd484439b3dc09cbdc979419679d402bd0a9409fbd`  
		Last Modified: Wed, 17 Nov 2021 12:13:55 GMT  
		Size: 55.3 MB (55349657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653d8908e660daa2a0615175ca8590b144cdd5aa6ee2652e83e6429ffee8cc47`  
		Last Modified: Wed, 17 Nov 2021 12:13:47 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:992c4786eeaa7c7d153d473fa819d9eb665c94790fc4ab000cbe46f774c16a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:e6f6804aecc2fb6b091c54021c1773b77968d798293d41ab3ee46f5c00a58bb1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58362658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7e9599575e47151d14b79975fd45baf80559233e36487f2ce8bbe0a941ce68`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:25:45 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:23:42 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Mon, 29 Nov 2021 18:23:42 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:23:42 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:23:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:23:43 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:23:43 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf619492e89f6485a3ba5e7cb6807f6f35a59e5715d4bffcb692cfecddeefbd8`  
		Last Modified: Mon, 29 Nov 2021 18:30:34 GMT  
		Size: 55.5 MB (55539197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a667c3f673f5f288f2ff0a45cd4743280d929515d6979127e0cb9f843854d03`  
		Last Modified: Mon, 29 Nov 2021 18:30:26 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:07a11ace7bd317e07641faf0290a9c424f2807c71c771ba4112352ed01edb825
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44182663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb5d3f39fab82aae82e0040de663009d9179c71d25aaa0f9f4f6c17dfd46917`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:41:33 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:43:01 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:43:02 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:43:03 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:43:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:43:03 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:43:04 GMT
CMD []
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6b7000342f95d46e5b48cfb7808d094fed8f3d82d54dbcae041ff5797e12e`  
		Last Modified: Sat, 13 Nov 2021 15:52:55 GMT  
		Size: 41.7 MB (41743567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9935ad4b54275bc2d461752cccef1d67e3625f43d41fca9f5f7fee10b0c581`  
		Last Modified: Sat, 13 Nov 2021 15:52:33 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:be906da2df7baeb35e33f21bb8b8569ca0cd3dcbf82f8325d387d409591e3341
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51108617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfad9e9cf640629bd0b7fe5970fbd652fb0450e6093adc58f4ae8781952b15c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:02:27 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 18:03:26 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 18:03:26 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 18:03:28 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:03:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 18:03:29 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 18:03:30 GMT
CMD []
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3156901f263be485231564efa49a95ae550f773936fcb146bc72ea32290ce733`  
		Last Modified: Fri, 12 Nov 2021 18:11:15 GMT  
		Size: 48.4 MB (48390438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5847cbe7d8162260bce419a5cb61ea09c1c93dc5e2bcd2b82d7e471fe269b907`  
		Last Modified: Fri, 12 Nov 2021 18:11:08 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:5197a57c34b3bd99ff5f8978737afc8422cd2c3f4c4b2622fc512c1bea56687c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58575907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b4da6c280c940a6fbe5cd93c6db63f23ba47e4de7ae74747c09ff56e2dd6af`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:27:36 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 20:29:32 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 20:29:33 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 20:29:33 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:29:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 20:29:34 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 20:29:35 GMT
CMD []
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2114eb284e1895354c615e8d675c2f51ea4b035086fe3990c5f7984bd37a0d`  
		Last Modified: Fri, 12 Nov 2021 20:38:38 GMT  
		Size: 55.7 MB (55744480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595cf1ed60723c431100d3228748183b34d9fec17114ef1d41f2e146a0172d58`  
		Last Modified: Fri, 12 Nov 2021 20:38:22 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:d01f07394fd2866aa545843ec1ff1e642d012d7b4c7cd9608e9dd481107b792e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48224608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2088057097d9716eee0d9dd9a041aa3ed9060a7a69fef1f35cf0ac516e0e8f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:52:07 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:53:18 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:53:23 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:53:23 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:53:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:53:27 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:53:32 GMT
CMD []
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f0b2c9903ecdaa15af2cabffb8e77f729da6dfd894a82938d64d8b6d92d630`  
		Last Modified: Sat, 13 Nov 2021 15:56:08 GMT  
		Size: 45.4 MB (45406662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53a44be231651b43f32bc477da875668dce263febec9ea0ac7dd322240fd334`  
		Last Modified: Sat, 13 Nov 2021 15:55:59 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ee47cf4c694d03327082b6ee67238206cd2586fd0122504982e334112691d7b5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46691858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf47f559ece084de3bd316f80ae674f00135b5b29d2922a5288c000964c8944`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:22 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 22:10:58 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=7.0.0/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 22:10:59 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 22:11:00 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:11:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 22:11:00 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 22:11:00 GMT
CMD []
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a59e55e723ec8fecb8ce8cac9c1ae3fd531846ef446d9f964d54ce8a381edc`  
		Last Modified: Fri, 12 Nov 2021 22:15:55 GMT  
		Size: 44.1 MB (44082103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483f8807a2f1038904772cff0766c6251ef9ed695640f95fa1a9807fed849c01`  
		Last Modified: Fri, 12 Nov 2021 22:15:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:275f630c142128fff6208ce00a2596d21d153cbe23ec8e7725fea4a14bac8fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:d3855cf0414ce764e06e30dd3ffda862b7aa3d68f86d98da40a9e7fc1587c7c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101190955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3658dee045ef52cd3218f3cc88c4e4a9cf4f9105d486b7aba50a70160087c42`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:02:38 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:22:36 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.1.tgz -o $tmpdir/orig.tgz;     echo "7541d50b03a113f0a13660d459cc4c2eb45d57fb19380ab56a5413a4e5d702f9c0856585f09aeea6084a239ad8c69017af3805a864540b4697e0eac29f00b408  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 29 Nov 2021 18:22:37 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:22:37 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:22:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:22:37 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:22:37 GMT
CMD []
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322bd05dea04ce119109555b9a65a488419a6aa963fb6d47943d7e34b78ba8b2`  
		Last Modified: Mon, 29 Nov 2021 18:30:11 GMT  
		Size: 69.8 MB (69820212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e3c589fc5a0354e3bdf0ff5d10e4a1f5e03a7ff4f2d790058ca309b1b1b7e9`  
		Last Modified: Mon, 29 Nov 2021 18:30:02 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c240e795e9d62cb28f000d79d4217892527ccb7ba16c15956f46f84eeaa6a041
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81217264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa82400ddb1489e132ea9fc08044a8414e5f6497bdd5d85f070d7213dd5d8be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 09:52:16 GMT
ENV VARNISH_SIZE=100M
# Thu, 18 Nov 2021 09:57:57 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 18 Nov 2021 09:57:58 GMT
WORKDIR /etc/varnish
# Thu, 18 Nov 2021 09:57:58 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Thu, 18 Nov 2021 09:57:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 18 Nov 2021 09:57:59 GMT
EXPOSE 80 8443
# Thu, 18 Nov 2021 09:58:00 GMT
CMD []
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995a81b2cb29588b95194d051d0db4ad26537aaf524bed3daa994739dbb67e27`  
		Last Modified: Thu, 18 Nov 2021 10:06:50 GMT  
		Size: 54.6 MB (54643631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0ad718cf28c5982b42621ef4bf65053b627878d4c49c7dde6b3f1dcfbe9156`  
		Last Modified: Thu, 18 Nov 2021 10:06:21 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:331e3ee5311aa4b31e5f8faacca07b84bd9173bfe5ba1e19e47148f862f09b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98702970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a951c912ec6ea48924d63ee40547975645660c14694ee1af097a24ffce7b149`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:32:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 04:34:37 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 04:34:38 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 04:34:39 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 04:34:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 04:34:40 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 04:34:41 GMT
CMD []
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eb9388ba1f805feffd8319d25466baeadd9f2d695f2aabc1b8444fc79cf250`  
		Last Modified: Wed, 17 Nov 2021 04:40:43 GMT  
		Size: 68.6 MB (68645975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e54176b0a037e66e61c824ba75ab82b47ba1e3e0fb2778c6a4e29c166e1a9a5`  
		Last Modified: Wed, 17 Nov 2021 04:40:33 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:50233d97f281820ca5abc37f58836a60ce0373326b786b9056f8171ce2d3f0f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105802766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fc2c2a2308e428482a33014c6cd52b1e77773c168972e9636c857d2eacf078`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:10:10 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 03:13:22 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 03:13:23 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 03:13:23 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 03:13:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 03:13:24 GMT
CMD []
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6da7e8bf779c7a01eff42003ce0234602d48047066bdae20757149f130940e`  
		Last Modified: Wed, 17 Nov 2021 03:18:12 GMT  
		Size: 73.4 MB (73421610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737ddd62e39b33ec70b8bda30309091c785af357bd9dbab9e8b71408188bfc2c`  
		Last Modified: Wed, 17 Nov 2021 03:17:58 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:9c1ea9b3990ca7a9106f0a8ec8b5cc38f4de5161912e2c2481a88b7459ba14f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103805146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ea3420500395a52f3cbbaa26ea64adacb99d5dce8f2e24baa6d1583465061f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:04:25 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 06:33:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 06:34:03 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 06:34:07 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 06:34:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 06:34:23 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 06:34:29 GMT
CMD []
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede74025f453eb239899d64b9466f119dc2f664e82b1529db59b5385dca93f18`  
		Last Modified: Wed, 17 Nov 2021 07:37:12 GMT  
		Size: 68.5 MB (68533289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab465f900cffa890ba81f5102d4613ced3e455e7c2ee38240330afd97d791da1`  
		Last Modified: Wed, 17 Nov 2021 07:36:59 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:e522646171effb2ec075821c7e8a8b1c60028f2d3203ed41d6b3da98e4e91dec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85001090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5981679e033a9ac77cd2b7a70bfbd08ca4c650d4dff4b879461ded143ea40d04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:09:56 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 12:11:39 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-7.0.0.tgz -o $tmpdir/orig.tgz;     echo "39c694db4ec7b35236d12fe2c03036260d6799395b1c8bb5a58e96fc88d67dcaa5eb8bc75643540d3aa0edc1a8924d7d839e88293b0521fadef4cd12f466fb4b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|7.0.0|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 12:11:41 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 12:11:41 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Wed, 17 Nov 2021 12:11:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 12:11:42 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 12:11:42 GMT
CMD []
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e14d21e5759658aedc62cd484439b3dc09cbdc979419679d402bd0a9409fbd`  
		Last Modified: Wed, 17 Nov 2021 12:13:55 GMT  
		Size: 55.3 MB (55349657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653d8908e660daa2a0615175ca8590b144cdd5aa6ee2652e83e6429ffee8cc47`  
		Last Modified: Wed, 17 Nov 2021 12:13:47 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old`

```console
$ docker pull varnish@sha256:d97bb2325f93e8f11840ec5dbbecfbe0f6eafe3c65065282812dfe818490f56c
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
$ docker pull varnish@sha256:14dc4591ca6ebc682192aeb88279148038ba1c80199db6734fd1ed3d9fe82ae1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101111708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9e2d7a898d88289a0dcaec28a767b263f436d22f9af49b303d94a3f22c9bcf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:02:38 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:26:15 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 29 Nov 2021 18:26:16 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:26:16 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:26:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:26:17 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:26:17 GMT
CMD []
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55795befb5cc32412c795a50fd294ec6bb72c993f58f3aa1e6aeb4b2632c353`  
		Last Modified: Mon, 29 Nov 2021 18:30:57 GMT  
		Size: 69.7 MB (69740739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74423f9b842a246e5b4d79beea3320392f0a3c0d50409eee98d13a45f799d6cc`  
		Last Modified: Mon, 29 Nov 2021 18:30:48 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:413095e503ec1943459aceac4700c136814ec9e17b0059fde00ac9f076071fe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80972534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f48b7cb9ce5481ed2e6b0ee90f2780f7772aa25e665040cdad90f309261a31`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 09:52:16 GMT
ENV VARNISH_SIZE=100M
# Fri, 19 Nov 2021 11:32:58 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 19 Nov 2021 11:32:59 GMT
WORKDIR /etc/varnish
# Fri, 19 Nov 2021 11:33:00 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 19 Nov 2021 11:33:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 19 Nov 2021 11:33:01 GMT
EXPOSE 80 8443
# Fri, 19 Nov 2021 11:33:01 GMT
CMD []
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534266287933de2f8a587d9c2e3042f8a900b0ebffe6b313d30640992031e493`  
		Last Modified: Fri, 19 Nov 2021 11:35:36 GMT  
		Size: 54.4 MB (54398673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16871c8ef77ec85d93ec5c3de00e0b395ed3989ad7df1de33f9362cd661f4bb`  
		Last Modified: Fri, 19 Nov 2021 11:35:07 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:978e2e9debb586c16e6b46ff7ac1cbfc1e701dc8e71a37ff931a8bead0921584
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98448784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98bdeeb4bc344b6d4e27f4f3f079484cd5638393e08449fd5072eb43bc20209`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:32:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 04:37:17 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 04:37:17 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 04:37:19 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 04:37:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 04:37:20 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 04:37:21 GMT
CMD []
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba02b5953ea5b80ba3c0ef84066635aceff7a0a8cb96f5006de1c134d4cb91e2`  
		Last Modified: Wed, 17 Nov 2021 04:41:12 GMT  
		Size: 68.4 MB (68391561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e4c378c0c18c653a37a0d63221a0d3b8ea4e6b25988e6c70fee20c761207bf`  
		Last Modified: Wed, 17 Nov 2021 04:41:02 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:f25bca95240699be6af700758548c536f9193baacea0b966888f3db09c93c515
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105580110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35352f71d5548760e4078ce33059d5dcb06bf29644007acd01ca4ede76822e16`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:10:10 GMT
ENV VARNISH_SIZE=100M
# Fri, 19 Nov 2021 02:15:39 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 19 Nov 2021 02:15:39 GMT
WORKDIR /etc/varnish
# Fri, 19 Nov 2021 02:15:40 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 19 Nov 2021 02:15:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 19 Nov 2021 02:15:40 GMT
EXPOSE 80 8443
# Fri, 19 Nov 2021 02:15:40 GMT
CMD []
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a3c0f8ad62670153755d6969ce97a978164c3f49fd4bd78fc717158fb43e8b`  
		Last Modified: Fri, 19 Nov 2021 02:17:05 GMT  
		Size: 73.2 MB (73198726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa39d65488c9d1db7318fb4ab937024de6b1eaf298ae2bba14594d052417bad`  
		Last Modified: Fri, 19 Nov 2021 02:16:50 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:e0b6433018298885884247c1c292bd869e42602b2f6cd74de6c6de55295d18ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103558961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2372a40b424a69707ffb97ae14efdbdec8dd2687bcbd9b8a571b5b710878da4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:04:25 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 07:08:18 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 07:08:24 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 07:08:26 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 07:08:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 07:08:33 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 07:08:38 GMT
CMD []
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9d0bd04f9bdd82973932c7ea0878410bce8db54b3dbf75aa1a8bdc94bca1c1`  
		Last Modified: Wed, 17 Nov 2021 07:37:44 GMT  
		Size: 68.3 MB (68286880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7348c6dc6d52c2df004d554143346a29441f83b45289c324aa9c08ebb8bb4a70`  
		Last Modified: Wed, 17 Nov 2021 07:37:31 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:14e377f6877ce74f254ed9ed95d31b7a40d16d4a62a987c4019e65d1d069301d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84737666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b27da94164283f11e04b01eaa1c5e0d71358b3249f3d1448574059b8cd14c53`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:09:56 GMT
ENV VARNISH_SIZE=100M
# Fri, 19 Nov 2021 02:11:05 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.6.1.tgz -o $tmpdir/orig.tgz;     echo "af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.6.1|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Fri, 19 Nov 2021 02:11:07 GMT
WORKDIR /etc/varnish
# Fri, 19 Nov 2021 02:11:07 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 19 Nov 2021 02:11:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 19 Nov 2021 02:11:07 GMT
EXPOSE 80 8443
# Fri, 19 Nov 2021 02:11:08 GMT
CMD []
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe324e886d9ee47afe369fd7b2c3c3e223f8213f286df5daa395bba36d378f`  
		Last Modified: Fri, 19 Nov 2021 02:12:35 GMT  
		Size: 55.1 MB (55086007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607c8fd5302cec2fa184d34ed2873b257df7dac3ba972aee15614765f9ffa43a`  
		Last Modified: Fri, 19 Nov 2021 02:12:28 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:91f0f0553f56f1ddb74d05d6603a53b566a45bdbeaeef4312284e44c2b5fbf62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:452898ec4382082c43e9aad4ad2313939833ac757ed3eedf122dd4107a060862
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57989509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9452c96edc1e2f1f4f52a9471093a1f653d6266bd8a9fae81849688342d1dfcd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:25:45 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:27:11 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder;
# Mon, 29 Nov 2021 18:27:11 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:27:11 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:27:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:27:12 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:27:12 GMT
CMD []
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153ae6d73742ceecdf942d8913c25adacffcf7590c180c52467774aae45fbdf8`  
		Last Modified: Mon, 29 Nov 2021 18:31:17 GMT  
		Size: 55.2 MB (55165820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47da88759d700deda407b20295e1fa1b16669b41d326a6ec602f1764725eb339`  
		Last Modified: Mon, 29 Nov 2021 18:31:09 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:aa0209cf51651473007d15a68a9e40b3ef78f01b0ca9a7b15a4465b34c44c6a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43832214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31d3ace99af9a9706f48dee76eb850e6812e89bf80a5d6a03b7f7443f000727`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:41:33 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:44:55 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:44:56 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:44:56 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:44:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:44:57 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:44:57 GMT
CMD []
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8cf867f2ac51813c0d1c016b3f20b0d9e83d4cbb126c3523cde64c96d7fcb4`  
		Last Modified: Sat, 13 Nov 2021 15:53:40 GMT  
		Size: 41.4 MB (41392891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabdbcc0379b966051181a7a466231d7e5acfefd771da959b5201467ecb927ce`  
		Last Modified: Sat, 13 Nov 2021 15:53:18 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dcad603946fbdbde3f8091aeadfec59a32593886d2a3677e06ec153999602c0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50731999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de07c78a7db786b0259191592ee3f133fe14e82e3771b98a2d89ae86740d7a04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:02:27 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 18:07:12 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 18:07:12 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 18:07:14 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:07:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 18:07:15 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 18:07:16 GMT
CMD []
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaeddc4ee611ed5f3b3af99a1d64e8a9fe9ac65234c10ae76b8f87c7408ee2c`  
		Last Modified: Fri, 12 Nov 2021 18:12:02 GMT  
		Size: 48.0 MB (48013591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb513dedceb393ae14a219dcc10e6ba648d1a3235cffeef2ba2fc580f7733e`  
		Last Modified: Fri, 12 Nov 2021 18:11:55 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:6cd7f5496daf8d5cee94d23598c0ca332ec68a0cdc177bc9709b499ceeb281a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58198355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4b96991872090e8a8b3365cb68ba0faacaa135080273c8f4c96827c4e83a85`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:27:36 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 20:31:59 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 20:31:59 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 20:32:00 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:32:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 20:32:01 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 20:32:01 GMT
CMD []
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2418aa38a4d46c393e749f3b79218139cf03e08ee533488eef7a184ba3c4b0`  
		Last Modified: Fri, 12 Nov 2021 20:39:20 GMT  
		Size: 55.4 MB (55366703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eafccd51cc8016d5729ab976a08c451c8129732ca52bd56dad9a9d33029d19`  
		Last Modified: Fri, 12 Nov 2021 20:39:03 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:11c9146decd9c1c86e757d6bf502754bb4aaa24f4ecc70f754f98a904a167f8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47835934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174b4a7f8e1f716e198b36dcdfb63151acded0a92bd8ed4e0af888921e7b9f70`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:52:07 GMT
ENV VARNISH_SIZE=100M
# Sat, 13 Nov 2021 15:54:52 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Sat, 13 Nov 2021 15:54:56 GMT
WORKDIR /etc/varnish
# Sat, 13 Nov 2021 15:54:57 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:55:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 13 Nov 2021 15:55:02 GMT
EXPOSE 80 8443
# Sat, 13 Nov 2021 15:55:05 GMT
CMD []
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf90faeee149fde78cbce6fe3ba8f350dae5b3d778c56fe8cf21f7659153baf`  
		Last Modified: Sat, 13 Nov 2021 15:56:35 GMT  
		Size: 45.0 MB (45017761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d7cbba8137c7532cd04b886d9b785fcc56268da21d5cc5984a3bc67bfcacc7`  
		Last Modified: Sat, 13 Nov 2021 15:56:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:e2259beb51b142852cfcd7c82fa2289c9142678927d47a596d3ebd7cddb587ed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46372437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ece1b0b0d9a917fbd44b1e04b59716b6e8830d12011d768b6ddff4949f1951`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:22 GMT
ENV VARNISH_SIZE=100M
# Fri, 12 Nov 2021 22:14:23 GMT
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo git";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout d3e6a3fad7d4c2ac781ada92dcc246e7eef9d129;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=6.6.1/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"af3ee1743af2ede2d3efbb73e5aa9b42c7bbd5f86163ec338c8afd1989c3e51ff3e1b40bed6b72224b5d339a74f22d6e5f3c3faf2fedee8ab4715307ed5d871b  varnish-\$pkgver.tgz\"/";     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";     chown builder -R .;     su builder -c "abuild -r";    apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;     apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache;     sed -i '/^builder/d' /etc/sudoers;     deluser --remove-home builder
# Fri, 12 Nov 2021 22:14:27 GMT
WORKDIR /etc/varnish
# Fri, 12 Nov 2021 22:14:27 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Fri, 12 Nov 2021 22:14:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 12 Nov 2021 22:14:28 GMT
EXPOSE 80 8443
# Fri, 12 Nov 2021 22:14:28 GMT
CMD []
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1189657b7eca29d2b12d6c4c882bb5f03f6963db35b11d4b1eb816062556f71d`  
		Last Modified: Fri, 12 Nov 2021 22:16:30 GMT  
		Size: 43.8 MB (43762453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400eaf2558f0a809c40ba38f6ed62ab3abb09026784e48d056e3c07e477bfa`  
		Last Modified: Fri, 12 Nov 2021 22:16:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:99de3ef66b51471e325b98d806e4589382c8067970027968cb8ab254fbfae161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:f1b99a76e21fcc1d5098783f161e5d8baae9f14a6b08b8210931415e7b413aec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100572810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aecc682cab2e96109a6d0ef8391b93f2f4ba92ce2b61702096dcf3fb8a5057`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:02:38 GMT
ENV VARNISH_SIZE=100M
# Mon, 29 Nov 2021 18:29:34 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 29 Nov 2021 18:29:34 GMT
WORKDIR /etc/varnish
# Mon, 29 Nov 2021 18:29:35 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Mon, 29 Nov 2021 18:29:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 29 Nov 2021 18:29:35 GMT
EXPOSE 80 8443
# Mon, 29 Nov 2021 18:29:35 GMT
CMD []
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd5a37ea8efe8f63cfc190a6128c5a382c13f7f68e6c37fe345ff78861a2553`  
		Last Modified: Mon, 29 Nov 2021 18:31:41 GMT  
		Size: 69.2 MB (69201839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d24281ccd4f88407de3ba98d9b6ff1a1d7cfc33c3e1326a6ac4902b571d82df`  
		Last Modified: Mon, 29 Nov 2021 18:31:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c07401fbada8dcfb30316530b22680d446cb206090d92fe1530bc8244876d941
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80045960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0575bdb28c3e85f2bec56215667be87aed7cf9da82997ae6cf0388b9920d5c3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 01:59:43 GMT
ADD file:cd2ac52107a2ea6657f23850a4b29366309eb39fa177321e0a9fd6d58562ae80 in / 
# Wed, 17 Nov 2021 01:59:44 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 09:52:16 GMT
ENV VARNISH_SIZE=100M
# Thu, 18 Nov 2021 10:05:04 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 18 Nov 2021 10:05:05 GMT
WORKDIR /etc/varnish
# Thu, 18 Nov 2021 10:05:05 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 18 Nov 2021 10:05:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 18 Nov 2021 10:05:06 GMT
EXPOSE 80 8443
# Thu, 18 Nov 2021 10:05:07 GMT
CMD []
```

-	Layers:
	-	`sha256:b6e5ca4da96841e58eb27c88695a059e5105fad5a066de803f4b94ae4002ba66`  
		Last Modified: Wed, 17 Nov 2021 02:15:13 GMT  
		Size: 26.6 MB (26573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5736611207f9ab6e495c3a8258205db6cf5c8dd58bbba8cf9058a1c3271b70c5`  
		Last Modified: Thu, 18 Nov 2021 10:07:47 GMT  
		Size: 53.5 MB (53472100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b70a0546c868480d128124ce89dc7923b8ce3979c92d7887f34cbc043b2267e`  
		Last Modified: Thu, 18 Nov 2021 10:07:19 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c928b550c26640919c0582045590d449f8ed4dde96d2aef96b9cc7c9ed409530
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97533085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04aad97694b8ac0c6fad4a40b9f56be76415697bd3c21381e912650779452d92`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 04:32:14 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 04:39:46 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 04:39:46 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 04:39:48 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 04:39:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 04:39:49 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 04:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ccc34b59256b34a663b30483f48ffe180875b7b9ab652ca6c5f086239106d2`  
		Last Modified: Wed, 17 Nov 2021 04:41:37 GMT  
		Size: 67.5 MB (67475863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ee133477d1347e016652a50cf39a47c1d9b619e1bcdbaefe5f26097572c7d9`  
		Last Modified: Wed, 17 Nov 2021 04:41:27 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:5d755ac59fca0f6e2c886e91cd66e4a1c18fbf9f67acd0ad7da6ebd23c2f8288
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104751828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90279c337e591d81685afdb3579485a9d53623da5cbd404029951f6901d0f1ab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:39:53 GMT
ADD file:ff018048717c0f5aa1730480d0bfea1c2bf94d6e2dae2d7cef46d05ffb0d93e1 in / 
# Wed, 17 Nov 2021 02:39:53 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:10:10 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 03:17:14 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 03:17:17 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 03:17:17 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 03:17:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 03:17:18 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 03:17:18 GMT
CMD []
```

-	Layers:
	-	`sha256:0bae0e1d4cb1d56ffeb9d05de7a097d3157267eef07b6d8131344d99bd97c431`  
		Last Modified: Wed, 17 Nov 2021 02:47:49 GMT  
		Size: 32.4 MB (32380683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cff288a3cfecf3065cb555da4033fd5136fa00c1d1a3fbaf2d26d86a654a042`  
		Last Modified: Wed, 17 Nov 2021 03:18:50 GMT  
		Size: 72.4 MB (72370444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b900b861bf9ebaa2a7a820a6b65a8e534f39d694b28f38933e74e384026298cf`  
		Last Modified: Wed, 17 Nov 2021 03:18:35 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:40cf090fa2b141c82b92a97999cb6e5edabfd8ca85ba937bd9d7b3634ce3f4bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102651397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591e633f06d21eec5a59ce9510e2695cc4082370f3d317fbed87d9c6713794d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 03:28:22 GMT
ADD file:5ed330f0fe1328f694fcaefb961cf4da4d8a4ff03100b21af718b69316168706 in / 
# Wed, 17 Nov 2021 03:28:38 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:04:25 GMT
ENV VARNISH_SIZE=100M
# Wed, 17 Nov 2021 07:36:01 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 17 Nov 2021 07:36:07 GMT
WORKDIR /etc/varnish
# Wed, 17 Nov 2021 07:36:08 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 17 Nov 2021 07:36:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 17 Nov 2021 07:36:11 GMT
EXPOSE 80 8443
# Wed, 17 Nov 2021 07:36:14 GMT
CMD []
```

-	Layers:
	-	`sha256:258ff2a13858db8f51b65662e02137c0abcfd2528ca73e92b7a40061d938fb1e`  
		Last Modified: Wed, 17 Nov 2021 03:54:34 GMT  
		Size: 35.3 MB (35271382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd72144f4cad756c9443b3fe38a48bb132072f786b8b8cf5dd94d6aac00175f6`  
		Last Modified: Wed, 17 Nov 2021 07:38:13 GMT  
		Size: 67.4 MB (67379313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26b3cef66f6a2e490527b4897674457868ceb0a192e3f9876834133cbcede80`  
		Last Modified: Wed, 17 Nov 2021 07:38:00 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:70f2c1561bd91312529d25d9060d1b6023f1e97a5d843a0af53f66845a91fcd4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83786925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d59abd0994117eb46de293abdc871becc1c4e79fa1e2a7177865c1066f96ec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 17 Nov 2021 02:42:27 GMT
ADD file:42f73dac307a6a5232e3100f3d3b36e8125f73a4ca504b106e60e2b66d242b2f in / 
# Wed, 17 Nov 2021 02:42:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 12:09:56 GMT
ENV VARNISH_SIZE=100M
# Wed, 24 Nov 2021 20:29:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f http://varnish-cache.org/_downloads/varnish-6.0.8.tgz -o $tmpdir/orig.tgz;     echo "73ed2f465ba3b11680b20a70633fc78da9b3eac68395f927b7ff02f4106b6cc92a2b395db2813a0605da2771530e5c4fc594eaf5a9a32bf2e42181b6dd90cf3f  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.8|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 24 Nov 2021 20:29:50 GMT
WORKDIR /etc/varnish
# Wed, 24 Nov 2021 20:29:50 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 24 Nov 2021 20:29:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 24 Nov 2021 20:29:50 GMT
EXPOSE 80 8443
# Wed, 24 Nov 2021 20:29:51 GMT
CMD []
```

-	Layers:
	-	`sha256:8d71e885edf612b507bbdcc48a970548d436b8709eeedfc2c98f6843a214b5e2`  
		Last Modified: Wed, 17 Nov 2021 02:48:25 GMT  
		Size: 29.7 MB (29650960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10c09fdaf917d59b135390e666871ffe70e2701d0e957686bdef300d8ccc837`  
		Last Modified: Wed, 24 Nov 2021 20:31:20 GMT  
		Size: 54.1 MB (54135264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e37af7af0efec3cdee9c3eaf78d448e442ebd292bd854fd2227521f177558b3`  
		Last Modified: Wed, 24 Nov 2021 20:31:13 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
