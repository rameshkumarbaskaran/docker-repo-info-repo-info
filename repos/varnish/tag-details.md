<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.11`](#varnish6011)
-	[`varnish:7.2`](#varnish72)
-	[`varnish:7.2-alpine`](#varnish72-alpine)
-	[`varnish:7.2.1`](#varnish721)
-	[`varnish:7.2.1-alpine`](#varnish721-alpine)
-	[`varnish:7.3`](#varnish73)
-	[`varnish:7.3-alpine`](#varnish73-alpine)
-	[`varnish:7.3.0`](#varnish730)
-	[`varnish:7.3.0-alpine`](#varnish730-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:fcf64330415f4e2dbae5116152341b21ca016778361f27e2e78cb8633fd58fb6
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
$ docker pull varnish@sha256:454bde26abe856c11f2c01e49ee4972295c529ca8d572cfd5ac7458c09dc7c6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100653611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bff958899eb177d68ddf3857432ca3caa2c29e9ac61fd74266988574660a054`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:42:01 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 08:44:02 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 08:44:03 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 08:44:03 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 08:44:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 08:44:03 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 08:44:03 GMT
CMD []
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ac5fdbdd5295f4e6ef96170d4b6072fdf64ef67b1fce4835037b8e91c3efc`  
		Last Modified: Thu, 23 Mar 2023 08:45:10 GMT  
		Size: 69.2 MB (69241506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d0a5f8d42b9a02bd2d685179c8010def08c6e8fb512917c1b65d918a108708`  
		Last Modified: Thu, 23 Mar 2023 08:45:01 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:aa0c080cc1b68eb694be57b394774e620d299b46e207685c03e249eb5e8f825f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77228234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7bcdaeade43ceb79e0ad2ce826942782ec2c48f3ab24bf6391af43b6ec472d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:33:43 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 12:35:40 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 12:35:40 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 12:35:41 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:35:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 12:35:41 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 12:35:41 GMT
CMD []
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5c7c592dd5fd3a325f43dc46c9e39c39c7d4794449157ba636890dc521693e`  
		Last Modified: Thu, 23 Mar 2023 12:36:44 GMT  
		Size: 50.7 MB (50650203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4cd2918617aa3fb3c34f6df728ce7c6d3c5008bcfe5ffad004354ccfba130d`  
		Last Modified: Thu, 23 Mar 2023 12:36:37 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:57ffc6a9acfa003a371ad0f81185cd8e35a1d03c963e6aef8bf3533763232a5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94715614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825eaf119d4795f7c54fd830d8e1b86f368d0809890c546995db8817ef82903f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:31:19 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:33:04 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 07:33:05 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:33:05 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:33:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:33:05 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:33:05 GMT
CMD []
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbe80000c70973cea6a6fa729ec97b0ede579e55bbaa11d96bc10fa1c819c2e`  
		Last Modified: Thu, 23 Mar 2023 07:34:03 GMT  
		Size: 64.7 MB (64652214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe7aba80bb8f6017efb994e2fe82ac30bf71b1729158636187278db132a9604`  
		Last Modified: Thu, 23 Mar 2023 07:33:56 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:c634b629b6af576f45d9b34884348979e02256af100ffd6601292658628883bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102080872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e480b2929c4a10c95ad4650a1b25a698b5deb5141a84e55d5f41c96b723a87d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:49:06 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 19:51:28 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 19:51:29 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 19:51:29 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:51:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 19:51:29 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 19:51:29 GMT
CMD []
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27296d9a8485bf51ab09c6030604be9818738e92acf93431ab9c2e11f2b6cddb`  
		Last Modified: Thu, 23 Mar 2023 19:52:56 GMT  
		Size: 69.7 MB (69683895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221df35ede9e1583031e7125c18605249d41d70d719ca12c66a36ea7f33232bd`  
		Last Modified: Thu, 23 Mar 2023 19:52:44 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:18bd3322c2f9ccc96bfce197018af7ff9306a5913379476af9c84e061e770095
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99803629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f0683fd328a003ec4c95f0c7d93bb88582d34cba7b9ea9a048b186914841c5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 Apr 2023 01:16:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 12 Apr 2023 01:16:52 GMT
WORKDIR /etc/varnish
# Wed, 12 Apr 2023 01:16:52 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:16:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 Apr 2023 01:16:53 GMT
EXPOSE 80 8443
# Wed, 12 Apr 2023 01:16:54 GMT
CMD []
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c91ede6f2abd53adaec518fad85de307f689c38e8eab390a7359e142ae3a16`  
		Last Modified: Wed, 12 Apr 2023 01:18:31 GMT  
		Size: 64.5 MB (64510930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd33a842deca9de4a3e249248620b5666ab2fa35cae6fe8b10b79955f955c3e`  
		Last Modified: Wed, 12 Apr 2023 01:18:15 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:69bd5fff0a8ca56a5c8272ac0f401cb954f762a2b6ad65a51a0cbccfff195261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81000136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d407fac676df9e15e1ff341197bbb641128b56d81f1cdf706502a3899e984ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:09:46 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:11:24 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 07:11:26 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:11:26 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:11:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:11:26 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:11:26 GMT
CMD []
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e74619a3634d4edc8b607a852318272e94e45a43dd1bc3100b88df9c04cba60`  
		Last Modified: Thu, 23 Mar 2023 07:12:18 GMT  
		Size: 51.4 MB (51352615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41672e050ea9a532388b3c2f5061371da1182a77e33f532128654fbd98fdc`  
		Last Modified: Thu, 23 Mar 2023 07:12:12 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.11`

```console
$ docker pull varnish@sha256:fcf64330415f4e2dbae5116152341b21ca016778361f27e2e78cb8633fd58fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.0.11` - linux; amd64

```console
$ docker pull varnish@sha256:454bde26abe856c11f2c01e49ee4972295c529ca8d572cfd5ac7458c09dc7c6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100653611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bff958899eb177d68ddf3857432ca3caa2c29e9ac61fd74266988574660a054`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:42:01 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 08:44:02 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 08:44:03 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 08:44:03 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 08:44:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 08:44:03 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 08:44:03 GMT
CMD []
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ac5fdbdd5295f4e6ef96170d4b6072fdf64ef67b1fce4835037b8e91c3efc`  
		Last Modified: Thu, 23 Mar 2023 08:45:10 GMT  
		Size: 69.2 MB (69241506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d0a5f8d42b9a02bd2d685179c8010def08c6e8fb512917c1b65d918a108708`  
		Last Modified: Thu, 23 Mar 2023 08:45:01 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.11` - linux; arm variant v7

```console
$ docker pull varnish@sha256:aa0c080cc1b68eb694be57b394774e620d299b46e207685c03e249eb5e8f825f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77228234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7bcdaeade43ceb79e0ad2ce826942782ec2c48f3ab24bf6391af43b6ec472d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:33:43 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 12:35:40 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 12:35:40 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 12:35:41 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:35:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 12:35:41 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 12:35:41 GMT
CMD []
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5c7c592dd5fd3a325f43dc46c9e39c39c7d4794449157ba636890dc521693e`  
		Last Modified: Thu, 23 Mar 2023 12:36:44 GMT  
		Size: 50.7 MB (50650203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4cd2918617aa3fb3c34f6df728ce7c6d3c5008bcfe5ffad004354ccfba130d`  
		Last Modified: Thu, 23 Mar 2023 12:36:37 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.11` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:57ffc6a9acfa003a371ad0f81185cd8e35a1d03c963e6aef8bf3533763232a5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94715614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825eaf119d4795f7c54fd830d8e1b86f368d0809890c546995db8817ef82903f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:31:19 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:33:04 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 07:33:05 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:33:05 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:33:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:33:05 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:33:05 GMT
CMD []
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbe80000c70973cea6a6fa729ec97b0ede579e55bbaa11d96bc10fa1c819c2e`  
		Last Modified: Thu, 23 Mar 2023 07:34:03 GMT  
		Size: 64.7 MB (64652214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe7aba80bb8f6017efb994e2fe82ac30bf71b1729158636187278db132a9604`  
		Last Modified: Thu, 23 Mar 2023 07:33:56 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.11` - linux; 386

```console
$ docker pull varnish@sha256:c634b629b6af576f45d9b34884348979e02256af100ffd6601292658628883bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102080872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e480b2929c4a10c95ad4650a1b25a698b5deb5141a84e55d5f41c96b723a87d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:49:06 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 19:51:28 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 19:51:29 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 19:51:29 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:51:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 19:51:29 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 19:51:29 GMT
CMD []
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27296d9a8485bf51ab09c6030604be9818738e92acf93431ab9c2e11f2b6cddb`  
		Last Modified: Thu, 23 Mar 2023 19:52:56 GMT  
		Size: 69.7 MB (69683895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221df35ede9e1583031e7125c18605249d41d70d719ca12c66a36ea7f33232bd`  
		Last Modified: Thu, 23 Mar 2023 19:52:44 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.11` - linux; ppc64le

```console
$ docker pull varnish@sha256:18bd3322c2f9ccc96bfce197018af7ff9306a5913379476af9c84e061e770095
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99803629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f0683fd328a003ec4c95f0c7d93bb88582d34cba7b9ea9a048b186914841c5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 Apr 2023 01:16:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 12 Apr 2023 01:16:52 GMT
WORKDIR /etc/varnish
# Wed, 12 Apr 2023 01:16:52 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:16:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 Apr 2023 01:16:53 GMT
EXPOSE 80 8443
# Wed, 12 Apr 2023 01:16:54 GMT
CMD []
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c91ede6f2abd53adaec518fad85de307f689c38e8eab390a7359e142ae3a16`  
		Last Modified: Wed, 12 Apr 2023 01:18:31 GMT  
		Size: 64.5 MB (64510930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd33a842deca9de4a3e249248620b5666ab2fa35cae6fe8b10b79955f955c3e`  
		Last Modified: Wed, 12 Apr 2023 01:18:15 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.11` - linux; s390x

```console
$ docker pull varnish@sha256:69bd5fff0a8ca56a5c8272ac0f401cb954f762a2b6ad65a51a0cbccfff195261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81000136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d407fac676df9e15e1ff341197bbb641128b56d81f1cdf706502a3899e984ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:09:46 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:11:24 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 07:11:26 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:11:26 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:11:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:11:26 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:11:26 GMT
CMD []
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e74619a3634d4edc8b607a852318272e94e45a43dd1bc3100b88df9c04cba60`  
		Last Modified: Thu, 23 Mar 2023 07:12:18 GMT  
		Size: 51.4 MB (51352615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41672e050ea9a532388b3c2f5061371da1182a77e33f532128654fbd98fdc`  
		Last Modified: Thu, 23 Mar 2023 07:12:12 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.2`

```console
$ docker pull varnish@sha256:8d70ffffd510634a21c7ecdf4a6b973b08232a9987bddd71a69d78770ab64952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.2` - linux; amd64

```console
$ docker pull varnish@sha256:51308e399b5bfb42c1acc656b5bb6593909e063e225d0194a72673bd68aba5b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106842482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8d5690ee4d009d1abc0f4765cc44d495ddcc5cf1c099161806ac0a9736aa75`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:39:07 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 08:39:07 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 08:39:07 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 08:39:07 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 08:39:07 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 08:41:46 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 08:41:46 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 08:41:46 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 08:41:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 08:41:46 GMT
USER varnish
# Thu, 23 Mar 2023 08:41:47 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 08:41:47 GMT
CMD []
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347377f781d4b09ab7508a61972fd4b3e5246b4e2bd9c35b6fd67626aa4fb2ab`  
		Last Modified: Thu, 23 Mar 2023 08:44:51 GMT  
		Size: 75.4 MB (75430587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3f25d148d89bd617db5fdf5fe5c6c6668b80541f6821f6d1b101c9b259b76`  
		Last Modified: Thu, 23 Mar 2023 08:44:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2` - linux; arm variant v7

```console
$ docker pull varnish@sha256:39f08af282e300bee400d681a13589ce486241507ceb777d1769ef79323686aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83187971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82615d9cab07301c0432d7198b5a1b74147212fb524a83b9881f9ae48bb5ab13`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:30:49 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 12:30:49 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 12:30:49 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 12:30:49 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 12:30:50 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 12:30:50 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 12:30:50 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 12:33:25 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 12:33:25 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 12:33:25 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:33:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 12:33:25 GMT
USER varnish
# Thu, 23 Mar 2023 12:33:26 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 12:33:26 GMT
CMD []
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138fb1bcb671938644266a2d6e0a35f5d781da8f3acfa8ec3b07f941e3c20cfd`  
		Last Modified: Thu, 23 Mar 2023 12:36:26 GMT  
		Size: 56.6 MB (56610150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecaa76a7918e4f17046b400bf59db8beb63a63bc17cb6ce56b7a9548f7bf8af`  
		Last Modified: Thu, 23 Mar 2023 12:36:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:266e9b50c88374c3169d686d798296050143e8fdb078a9cd5953a573a7d62f6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100868360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e23fa80f9496e9f34877c07b18fe4710a89f6d7f7c5daccfa8891adcb970433`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:28:56 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 07:28:56 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 07:28:56 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:28:57 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:28:57 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:31:16 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:31:16 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:31:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:31:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:31:17 GMT
USER varnish
# Thu, 23 Mar 2023 07:31:17 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:31:17 GMT
CMD []
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25386ca99e6fa25d37d6be5b3c0712ff9cccffb73dc9ce32937bb13dc65999b7`  
		Last Modified: Thu, 23 Mar 2023 07:33:46 GMT  
		Size: 70.8 MB (70805167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88ce616ecea4f7377751a315243e6fd13702ec941bfeb1254732c6c14cb7f38`  
		Last Modified: Thu, 23 Mar 2023 07:33:39 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2` - linux; 386

```console
$ docker pull varnish@sha256:c5847816dbbba69f71abce18fe4e24d6884a124c2f34ed0ad714b0547784056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108227006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfc7fdeefdec180ace517aae569c98d739b6bbbc071ac199b6c96b3a43e1e6b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:45:42 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 19:45:42 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 19:45:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 19:45:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 19:45:43 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 19:45:43 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 19:45:43 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 19:49:01 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 19:49:02 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 19:49:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:49:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 19:49:02 GMT
USER varnish
# Thu, 23 Mar 2023 19:49:02 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 19:49:02 GMT
CMD []
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a361541ee32822f6a5bcc2a2f6f08634cfe9d2cbc9b31e6ff456e3ac1488bc`  
		Last Modified: Thu, 23 Mar 2023 19:52:34 GMT  
		Size: 75.8 MB (75830240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37baffbfd4dfac65be48e4991e66887a684b81abc578406df0cea4592e054b91`  
		Last Modified: Thu, 23 Mar 2023 19:52:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2` - linux; ppc64le

```console
$ docker pull varnish@sha256:2ddbd11558d86d08b3f82a25da574d70734fed468550edb4d6b957cf2fc4ff55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106112382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fcc671da9acaf8ae312a5ba85fd3d77e7e1b88a900054ac23433f6dad4b7cde`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:55:40 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Wed, 12 Apr 2023 00:55:40 GMT
ARG VARNISH_VERSION=7.2.1
# Wed, 12 Apr 2023 00:55:41 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Wed, 12 Apr 2023 00:55:41 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Wed, 12 Apr 2023 00:55:42 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Wed, 12 Apr 2023 00:55:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 12 Apr 2023 00:55:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Wed, 12 Apr 2023 00:55:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Wed, 12 Apr 2023 00:55:44 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 12 Apr 2023 00:55:45 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Wed, 12 Apr 2023 00:55:45 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 Apr 2023 01:06:37 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 12 Apr 2023 01:06:41 GMT
WORKDIR /etc/varnish
# Wed, 12 Apr 2023 01:06:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:06:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 Apr 2023 01:06:43 GMT
USER varnish
# Wed, 12 Apr 2023 01:06:43 GMT
EXPOSE 80 8443
# Wed, 12 Apr 2023 01:06:45 GMT
CMD []
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4a89d7f741d3117b0ee6c2f7194da63a2eb7e31a212514121c21a0f9a2d56d`  
		Last Modified: Wed, 12 Apr 2023 01:18:03 GMT  
		Size: 70.8 MB (70819898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3fec9bc4ead77e694d7ee941f4809ba1dc75a4379c2e14982a287a907f61d2`  
		Last Modified: Wed, 12 Apr 2023 01:17:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2` - linux; s390x

```console
$ docker pull varnish@sha256:a828400ea054dd296391072926707f18eb07be46812e335f5171c1cb838621b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87138814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382ad2c68c00cbb928f0c3c2bdc525e23bbeb36107ce85428f3155f0525265da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:07:08 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 07:07:09 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 07:07:09 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:07:09 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:07:09 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:09:29 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:09:32 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:09:32 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:09:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:09:32 GMT
USER varnish
# Thu, 23 Mar 2023 07:09:32 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c80f77587a5dfe7c42be2aa5ec37fb62f7b9e9b8d92f302c306132a915684e`  
		Last Modified: Thu, 23 Mar 2023 07:12:05 GMT  
		Size: 57.5 MB (57491504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2feadb32de32ec44136c747758376b15f1fcd05d3cabc73325bbf1eb070b33`  
		Last Modified: Thu, 23 Mar 2023 07:11:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.2-alpine`

```console
$ docker pull varnish@sha256:4afc17b0aa7c483b822ae0c548f93d87fdcfc38715e30734657bad8a3171f534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.2-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:a320ad063c3556dfea1308e7747a7b74de2e6580bb136653f10480b192d2b7ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59399546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619a779899e4b887658162b42b9f51b181570836a20e93eabacd1c0634421c23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:16:18 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 02:16:18 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 02:16:18 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 02:16:19 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 02:16:19 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 02:16:19 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 02:17:35 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 02:17:35 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 02:17:35 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 02:17:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 02:17:35 GMT
USER varnish
# Thu, 30 Mar 2023 02:17:35 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 02:17:36 GMT
CMD []
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c114fe4204a2c955105dd5cd8a42a772594a1642947fbefba511406b0e60e5`  
		Last Modified: Thu, 30 Mar 2023 02:18:20 GMT  
		Size: 56.6 MB (56572454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debea196e0761731bed241b5b0124d7dab6070192ebf9f49532117ef228a4fd7`  
		Last Modified: Thu, 30 Mar 2023 02:18:13 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:fccf7f20e1622e5cc7de9c8a0374d530f4ce08e15bae3fa806e6c5f34100a250
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ac3c9362d31494b1482831d5f9600db9a9423084b5bcdfb6bf502d29be4134`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:05:06 GMT
ADD file:0516b2e2d8a5c0a3e85e67a20375312bdc586a63094d779b9ac92517cf74a19d in / 
# Wed, 29 Mar 2023 18:05:06 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:16:02 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 00:16:02 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 00:16:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 00:16:03 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 00:16:03 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 00:16:03 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 00:17:15 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 00:17:16 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 00:17:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 00:17:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 00:17:16 GMT
USER varnish
# Thu, 30 Mar 2023 00:17:16 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 00:17:16 GMT
CMD []
```

-	Layers:
	-	`sha256:fafb00bc68cf26e4a27ad2dce7303945ba9e40994e77c9269e610e0452ae9dce`  
		Last Modified: Wed, 29 Mar 2023 18:07:17 GMT  
		Size: 2.4 MB (2437606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7ec1086689ab0fd73293e70d501d454a27eb5ea261d03a2430cb0d14696427`  
		Last Modified: Sat, 08 Apr 2023 02:41:03 GMT  
		Size: 42.7 MB (42710102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9ac18a355d90f33336fbada96e19569338d541feae42ae2d313ce006609bb1`  
		Last Modified: Sat, 08 Apr 2023 02:40:57 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4b01c566b91d765af9c55ca58772d6926b481ba4c60bfe7b9d6b0adca255f10b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52139702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3552cf8b859208887e19e7d4ff64ae304e14cf411f5dadeb80d6c52b607f72d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:55:19 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 05:55:20 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 05:55:20 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 05:55:20 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 05:55:20 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 05:56:25 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 05:56:25 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 05:56:25 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 05:56:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 05:56:26 GMT
USER varnish
# Thu, 30 Mar 2023 05:56:26 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 05:56:26 GMT
CMD []
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c53d05c94805192159ec306400f8402f101647b10b4f2862a4b9cafe6d9ea95`  
		Last Modified: Thu, 30 Mar 2023 05:57:04 GMT  
		Size: 49.4 MB (49417204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfbbc1899969f2944b32d817962c27670200b641a7ff5b382026a2a6f1e91f8`  
		Last Modified: Thu, 30 Mar 2023 05:56:58 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b4aed57dfb69759cbbf97f8251f733ed209e5377c0b138e878768446cf3f1012
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59579474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2d5054f0237342f09e7c81d57f5b91b2a7258c98c54862bcd60b70f213eff4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:36:10 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 01:36:10 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 01:36:11 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 01:36:11 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 01:36:11 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 01:38:03 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 01:38:03 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 01:38:03 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 01:38:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 01:38:03 GMT
USER varnish
# Thu, 30 Mar 2023 01:38:04 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 01:38:04 GMT
CMD []
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec17ca4c36e5d196286fcd4f66f0a6879ff35841617edc48c24a2b0d3fed6c5`  
		Last Modified: Thu, 30 Mar 2023 01:39:02 GMT  
		Size: 56.7 MB (56746401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acb1c0b2cc2ca1f40568c89f6ace8d204192474b0b299f6afbd1d5b87c89ad4`  
		Last Modified: Thu, 30 Mar 2023 01:38:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:47175a4b9a3d7cc10400bda61c20d308651152bf93f3268aa3b4c850c4cebb3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49172829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe520b41ef8593a0ca87c4b15e445248e7728729026968d7c7167a33b40a8e28`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:16:40 GMT
ADD file:3c2a8d553fa0998f13f86592f104a9a4ad14f8db46dfa9145c8fbbca0b87ee9a in / 
# Wed, 29 Mar 2023 18:16:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:35:48 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 04:35:48 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 04:35:49 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 04:35:49 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 04:35:49 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 04:35:50 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 04:35:50 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 04:35:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 04:35:51 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 04:35:51 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 04:35:51 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 04:37:42 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 04:37:43 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 04:37:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 04:37:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 04:37:44 GMT
USER varnish
# Thu, 30 Mar 2023 04:37:45 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 04:37:45 GMT
CMD []
```

-	Layers:
	-	`sha256:0b40b0bd0da3095d93bf74233a1d0bf638b2511fee461df8f6a71aad5a038589`  
		Last Modified: Wed, 29 Mar 2023 18:17:38 GMT  
		Size: 2.8 MB (2813760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69361e01f667423c0f2d961984f6e7db1a81226574e2f2e13b25de56a1ed714d`  
		Last Modified: Thu, 30 Mar 2023 04:38:48 GMT  
		Size: 46.4 MB (46358574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b033b092d98a898fd606406859a2bdc093c0babde613a26ed82fff5736c9290`  
		Last Modified: Thu, 30 Mar 2023 04:38:37 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:cae32a9f29cd9997a1fe2ee6f8d0b8e3ff91c21e6213716d9ac34675317dc70d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47646967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e24f77bba538e7715318a014e47a2ab4183cd521c07f85ecc3a82ab13ed2830`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:42:07 GMT
ADD file:5cf392863cd9a0735de88f9e7dab93c9e74aca59ca05b792943cf3b621ea2c59 in / 
# Wed, 29 Mar 2023 17:42:07 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 23:10:06 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VARNISH_VERSION=7.2.1
# Wed, 29 Mar 2023 23:10:06 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Wed, 29 Mar 2023 23:10:07 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 29 Mar 2023 23:10:07 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Wed, 29 Mar 2023 23:10:07 GMT
ENV VARNISH_SIZE=100M
# Wed, 29 Mar 2023 23:11:26 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Wed, 29 Mar 2023 23:11:28 GMT
WORKDIR /etc/varnish
# Wed, 29 Mar 2023 23:11:28 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 29 Mar 2023 23:11:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 29 Mar 2023 23:11:28 GMT
USER varnish
# Wed, 29 Mar 2023 23:11:28 GMT
EXPOSE 80 8443
# Wed, 29 Mar 2023 23:11:28 GMT
CMD []
```

-	Layers:
	-	`sha256:1536575ac9c5f5fff4522c60d4610af0a52be584c36e652080c6c0ad169d4f27`  
		Last Modified: Wed, 29 Mar 2023 17:42:42 GMT  
		Size: 2.6 MB (2610636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091447cbd58b57bbe1eb2edf62b5e2d9c06467104aebfc70c02d7cfafa01868c`  
		Last Modified: Wed, 29 Mar 2023 23:12:17 GMT  
		Size: 45.0 MB (45035834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390574d541f53e2036c226ec79255c18a2429053de04847092de875c4925890b`  
		Last Modified: Wed, 29 Mar 2023 23:12:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.2.1`

```console
$ docker pull varnish@sha256:8d70ffffd510634a21c7ecdf4a6b973b08232a9987bddd71a69d78770ab64952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.2.1` - linux; amd64

```console
$ docker pull varnish@sha256:51308e399b5bfb42c1acc656b5bb6593909e063e225d0194a72673bd68aba5b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106842482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8d5690ee4d009d1abc0f4765cc44d495ddcc5cf1c099161806ac0a9736aa75`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:39:07 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 08:39:07 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 08:39:07 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 08:39:07 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 08:39:07 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 08:41:46 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 08:41:46 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 08:41:46 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 08:41:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 08:41:46 GMT
USER varnish
# Thu, 23 Mar 2023 08:41:47 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 08:41:47 GMT
CMD []
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347377f781d4b09ab7508a61972fd4b3e5246b4e2bd9c35b6fd67626aa4fb2ab`  
		Last Modified: Thu, 23 Mar 2023 08:44:51 GMT  
		Size: 75.4 MB (75430587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3f25d148d89bd617db5fdf5fe5c6c6668b80541f6821f6d1b101c9b259b76`  
		Last Modified: Thu, 23 Mar 2023 08:44:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:39f08af282e300bee400d681a13589ce486241507ceb777d1769ef79323686aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83187971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82615d9cab07301c0432d7198b5a1b74147212fb524a83b9881f9ae48bb5ab13`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:30:49 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 12:30:49 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 12:30:49 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 12:30:49 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 12:30:50 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 12:30:50 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 12:30:50 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 12:33:25 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 12:33:25 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 12:33:25 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:33:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 12:33:25 GMT
USER varnish
# Thu, 23 Mar 2023 12:33:26 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 12:33:26 GMT
CMD []
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138fb1bcb671938644266a2d6e0a35f5d781da8f3acfa8ec3b07f941e3c20cfd`  
		Last Modified: Thu, 23 Mar 2023 12:36:26 GMT  
		Size: 56.6 MB (56610150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecaa76a7918e4f17046b400bf59db8beb63a63bc17cb6ce56b7a9548f7bf8af`  
		Last Modified: Thu, 23 Mar 2023 12:36:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:266e9b50c88374c3169d686d798296050143e8fdb078a9cd5953a573a7d62f6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100868360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e23fa80f9496e9f34877c07b18fe4710a89f6d7f7c5daccfa8891adcb970433`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:28:56 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 07:28:56 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 07:28:56 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:28:57 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:28:57 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:31:16 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:31:16 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:31:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:31:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:31:17 GMT
USER varnish
# Thu, 23 Mar 2023 07:31:17 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:31:17 GMT
CMD []
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25386ca99e6fa25d37d6be5b3c0712ff9cccffb73dc9ce32937bb13dc65999b7`  
		Last Modified: Thu, 23 Mar 2023 07:33:46 GMT  
		Size: 70.8 MB (70805167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88ce616ecea4f7377751a315243e6fd13702ec941bfeb1254732c6c14cb7f38`  
		Last Modified: Thu, 23 Mar 2023 07:33:39 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2.1` - linux; 386

```console
$ docker pull varnish@sha256:c5847816dbbba69f71abce18fe4e24d6884a124c2f34ed0ad714b0547784056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108227006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfc7fdeefdec180ace517aae569c98d739b6bbbc071ac199b6c96b3a43e1e6b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:45:42 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 19:45:42 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 19:45:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 19:45:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 19:45:43 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 19:45:43 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 19:45:43 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 19:49:01 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 19:49:02 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 19:49:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:49:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 19:49:02 GMT
USER varnish
# Thu, 23 Mar 2023 19:49:02 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 19:49:02 GMT
CMD []
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a361541ee32822f6a5bcc2a2f6f08634cfe9d2cbc9b31e6ff456e3ac1488bc`  
		Last Modified: Thu, 23 Mar 2023 19:52:34 GMT  
		Size: 75.8 MB (75830240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37baffbfd4dfac65be48e4991e66887a684b81abc578406df0cea4592e054b91`  
		Last Modified: Thu, 23 Mar 2023 19:52:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:2ddbd11558d86d08b3f82a25da574d70734fed468550edb4d6b957cf2fc4ff55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106112382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fcc671da9acaf8ae312a5ba85fd3d77e7e1b88a900054ac23433f6dad4b7cde`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:55:40 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Wed, 12 Apr 2023 00:55:40 GMT
ARG VARNISH_VERSION=7.2.1
# Wed, 12 Apr 2023 00:55:41 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Wed, 12 Apr 2023 00:55:41 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Wed, 12 Apr 2023 00:55:42 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Wed, 12 Apr 2023 00:55:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 12 Apr 2023 00:55:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Wed, 12 Apr 2023 00:55:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Wed, 12 Apr 2023 00:55:44 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 12 Apr 2023 00:55:45 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Wed, 12 Apr 2023 00:55:45 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 Apr 2023 01:06:37 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 12 Apr 2023 01:06:41 GMT
WORKDIR /etc/varnish
# Wed, 12 Apr 2023 01:06:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:06:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 Apr 2023 01:06:43 GMT
USER varnish
# Wed, 12 Apr 2023 01:06:43 GMT
EXPOSE 80 8443
# Wed, 12 Apr 2023 01:06:45 GMT
CMD []
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4a89d7f741d3117b0ee6c2f7194da63a2eb7e31a212514121c21a0f9a2d56d`  
		Last Modified: Wed, 12 Apr 2023 01:18:03 GMT  
		Size: 70.8 MB (70819898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3fec9bc4ead77e694d7ee941f4809ba1dc75a4379c2e14982a287a907f61d2`  
		Last Modified: Wed, 12 Apr 2023 01:17:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2.1` - linux; s390x

```console
$ docker pull varnish@sha256:a828400ea054dd296391072926707f18eb07be46812e335f5171c1cb838621b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87138814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382ad2c68c00cbb928f0c3c2bdc525e23bbeb36107ce85428f3155f0525265da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:07:08 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 07:07:09 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 07:07:09 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:07:09 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:07:09 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:09:29 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:09:32 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:09:32 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:09:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:09:32 GMT
USER varnish
# Thu, 23 Mar 2023 07:09:32 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c80f77587a5dfe7c42be2aa5ec37fb62f7b9e9b8d92f302c306132a915684e`  
		Last Modified: Thu, 23 Mar 2023 07:12:05 GMT  
		Size: 57.5 MB (57491504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2feadb32de32ec44136c747758376b15f1fcd05d3cabc73325bbf1eb070b33`  
		Last Modified: Thu, 23 Mar 2023 07:11:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.2.1-alpine`

```console
$ docker pull varnish@sha256:4afc17b0aa7c483b822ae0c548f93d87fdcfc38715e30734657bad8a3171f534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.2.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:a320ad063c3556dfea1308e7747a7b74de2e6580bb136653f10480b192d2b7ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59399546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619a779899e4b887658162b42b9f51b181570836a20e93eabacd1c0634421c23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:16:18 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 02:16:18 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 02:16:18 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 02:16:19 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 02:16:19 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 02:16:19 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 02:17:35 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 02:17:35 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 02:17:35 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 02:17:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 02:17:35 GMT
USER varnish
# Thu, 30 Mar 2023 02:17:35 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 02:17:36 GMT
CMD []
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c114fe4204a2c955105dd5cd8a42a772594a1642947fbefba511406b0e60e5`  
		Last Modified: Thu, 30 Mar 2023 02:18:20 GMT  
		Size: 56.6 MB (56572454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debea196e0761731bed241b5b0124d7dab6070192ebf9f49532117ef228a4fd7`  
		Last Modified: Thu, 30 Mar 2023 02:18:13 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:fccf7f20e1622e5cc7de9c8a0374d530f4ce08e15bae3fa806e6c5f34100a250
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ac3c9362d31494b1482831d5f9600db9a9423084b5bcdfb6bf502d29be4134`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:05:06 GMT
ADD file:0516b2e2d8a5c0a3e85e67a20375312bdc586a63094d779b9ac92517cf74a19d in / 
# Wed, 29 Mar 2023 18:05:06 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:16:02 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 00:16:02 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 00:16:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 00:16:03 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 00:16:03 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 00:16:03 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 00:17:15 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 00:17:16 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 00:17:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 00:17:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 00:17:16 GMT
USER varnish
# Thu, 30 Mar 2023 00:17:16 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 00:17:16 GMT
CMD []
```

-	Layers:
	-	`sha256:fafb00bc68cf26e4a27ad2dce7303945ba9e40994e77c9269e610e0452ae9dce`  
		Last Modified: Wed, 29 Mar 2023 18:07:17 GMT  
		Size: 2.4 MB (2437606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7ec1086689ab0fd73293e70d501d454a27eb5ea261d03a2430cb0d14696427`  
		Last Modified: Sat, 08 Apr 2023 02:41:03 GMT  
		Size: 42.7 MB (42710102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9ac18a355d90f33336fbada96e19569338d541feae42ae2d313ce006609bb1`  
		Last Modified: Sat, 08 Apr 2023 02:40:57 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4b01c566b91d765af9c55ca58772d6926b481ba4c60bfe7b9d6b0adca255f10b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52139702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3552cf8b859208887e19e7d4ff64ae304e14cf411f5dadeb80d6c52b607f72d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:55:19 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 05:55:20 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 05:55:20 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 05:55:20 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 05:55:20 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 05:56:25 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 05:56:25 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 05:56:25 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 05:56:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 05:56:26 GMT
USER varnish
# Thu, 30 Mar 2023 05:56:26 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 05:56:26 GMT
CMD []
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c53d05c94805192159ec306400f8402f101647b10b4f2862a4b9cafe6d9ea95`  
		Last Modified: Thu, 30 Mar 2023 05:57:04 GMT  
		Size: 49.4 MB (49417204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfbbc1899969f2944b32d817962c27670200b641a7ff5b382026a2a6f1e91f8`  
		Last Modified: Thu, 30 Mar 2023 05:56:58 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b4aed57dfb69759cbbf97f8251f733ed209e5377c0b138e878768446cf3f1012
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59579474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2d5054f0237342f09e7c81d57f5b91b2a7258c98c54862bcd60b70f213eff4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:36:10 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 01:36:10 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 01:36:11 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 01:36:11 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 01:36:11 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 01:38:03 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 01:38:03 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 01:38:03 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 01:38:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 01:38:03 GMT
USER varnish
# Thu, 30 Mar 2023 01:38:04 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 01:38:04 GMT
CMD []
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec17ca4c36e5d196286fcd4f66f0a6879ff35841617edc48c24a2b0d3fed6c5`  
		Last Modified: Thu, 30 Mar 2023 01:39:02 GMT  
		Size: 56.7 MB (56746401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acb1c0b2cc2ca1f40568c89f6ace8d204192474b0b299f6afbd1d5b87c89ad4`  
		Last Modified: Thu, 30 Mar 2023 01:38:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:47175a4b9a3d7cc10400bda61c20d308651152bf93f3268aa3b4c850c4cebb3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49172829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe520b41ef8593a0ca87c4b15e445248e7728729026968d7c7167a33b40a8e28`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:16:40 GMT
ADD file:3c2a8d553fa0998f13f86592f104a9a4ad14f8db46dfa9145c8fbbca0b87ee9a in / 
# Wed, 29 Mar 2023 18:16:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:35:48 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 04:35:48 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 04:35:49 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 04:35:49 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 04:35:49 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 04:35:50 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 04:35:50 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 04:35:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 04:35:51 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 04:35:51 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 04:35:51 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 04:37:42 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 04:37:43 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 04:37:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 04:37:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 04:37:44 GMT
USER varnish
# Thu, 30 Mar 2023 04:37:45 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 04:37:45 GMT
CMD []
```

-	Layers:
	-	`sha256:0b40b0bd0da3095d93bf74233a1d0bf638b2511fee461df8f6a71aad5a038589`  
		Last Modified: Wed, 29 Mar 2023 18:17:38 GMT  
		Size: 2.8 MB (2813760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69361e01f667423c0f2d961984f6e7db1a81226574e2f2e13b25de56a1ed714d`  
		Last Modified: Thu, 30 Mar 2023 04:38:48 GMT  
		Size: 46.4 MB (46358574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b033b092d98a898fd606406859a2bdc093c0babde613a26ed82fff5736c9290`  
		Last Modified: Thu, 30 Mar 2023 04:38:37 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.2.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:cae32a9f29cd9997a1fe2ee6f8d0b8e3ff91c21e6213716d9ac34675317dc70d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47646967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e24f77bba538e7715318a014e47a2ab4183cd521c07f85ecc3a82ab13ed2830`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:42:07 GMT
ADD file:5cf392863cd9a0735de88f9e7dab93c9e74aca59ca05b792943cf3b621ea2c59 in / 
# Wed, 29 Mar 2023 17:42:07 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 23:10:06 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VARNISH_VERSION=7.2.1
# Wed, 29 Mar 2023 23:10:06 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Wed, 29 Mar 2023 23:10:07 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 29 Mar 2023 23:10:07 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Wed, 29 Mar 2023 23:10:07 GMT
ENV VARNISH_SIZE=100M
# Wed, 29 Mar 2023 23:11:26 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Wed, 29 Mar 2023 23:11:28 GMT
WORKDIR /etc/varnish
# Wed, 29 Mar 2023 23:11:28 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 29 Mar 2023 23:11:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 29 Mar 2023 23:11:28 GMT
USER varnish
# Wed, 29 Mar 2023 23:11:28 GMT
EXPOSE 80 8443
# Wed, 29 Mar 2023 23:11:28 GMT
CMD []
```

-	Layers:
	-	`sha256:1536575ac9c5f5fff4522c60d4610af0a52be584c36e652080c6c0ad169d4f27`  
		Last Modified: Wed, 29 Mar 2023 17:42:42 GMT  
		Size: 2.6 MB (2610636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091447cbd58b57bbe1eb2edf62b5e2d9c06467104aebfc70c02d7cfafa01868c`  
		Last Modified: Wed, 29 Mar 2023 23:12:17 GMT  
		Size: 45.0 MB (45035834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390574d541f53e2036c226ec79255c18a2429053de04847092de875c4925890b`  
		Last Modified: Wed, 29 Mar 2023 23:12:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3`

```console
$ docker pull varnish@sha256:2f211fd175cf8d3b2803abe0bcc1b42a94c2557568e4f301340f18c517254acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.3` - linux; amd64

```console
$ docker pull varnish@sha256:966e57e0f907166e5cfe74f03c70027a7bfeb7763d21ef6c0421f62415e9cde0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106798860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde7e0fae0241ca1def63efb79171503518a8488438150538534de27d6aa8e8e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:35:42 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 08:35:43 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 08:35:43 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 08:35:43 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 08:38:51 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 08:38:52 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 08:38:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 08:38:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 08:38:52 GMT
USER varnish
# Thu, 23 Mar 2023 08:38:52 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 08:38:52 GMT
CMD []
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ebc78fcc0bfd5f9a86a59c7ba9dc92d6c6ac286ed8792d8616139b3f728557`  
		Last Modified: Thu, 23 Mar 2023 08:44:29 GMT  
		Size: 75.4 MB (75386965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3679bcba66926e3e08e43f6a3b27ae9c5902dca3a35c8a3b5c4da60d413ff28d`  
		Last Modified: Thu, 23 Mar 2023 08:44:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e853c6bce2a44d87519a8074817ef212fab243e6dd356a4abd7e512d7067617c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83146210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad755a8b29b5be4bc688f975df90490adc469fb52f225c1498c7796c7647faf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:27:26 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 12:27:26 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 12:27:26 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 12:27:27 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 12:30:37 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 12:30:37 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 12:30:38 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:30:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 12:30:38 GMT
USER varnish
# Thu, 23 Mar 2023 12:30:38 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 12:30:38 GMT
CMD []
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e2d8b662d5f484247a6608121d266efd1a66ababf38e85884f4b25c943a1b`  
		Last Modified: Thu, 23 Mar 2023 12:36:07 GMT  
		Size: 56.6 MB (56568388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e95c1272c5b14b209ef35f4b8e7b15c931bf708123d990755924aa025813cc`  
		Last Modified: Thu, 23 Mar 2023 12:36:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e5c5ffd6dc2c95d7fee3e5bcbf2d300bb9b0f33918460846e02bb0bc789617c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100588684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720135e26f679dcaa1eeddcd6ae73bb0c8c9cda47e9f248bc72656427f8d3bb5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:25:32 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 07:25:32 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 07:25:33 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:25:33 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:25:33 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:28:40 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:28:40 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:28:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:28:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:28:40 GMT
USER varnish
# Thu, 23 Mar 2023 07:28:40 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:28:41 GMT
CMD []
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88629f01162d8c785683ae0fbde30f240c471df8fb8aad45c270bea1517206`  
		Last Modified: Thu, 23 Mar 2023 07:33:28 GMT  
		Size: 70.5 MB (70525493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132c73bad44c61b38ee1ac99c3b7cbcedeb6aaf28804afc1b2f5e9cc4240a43`  
		Last Modified: Thu, 23 Mar 2023 07:33:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; 386

```console
$ docker pull varnish@sha256:d419b0f75d76108ac53df1fb2fe379af01c91466546b17a14308403e11c46a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108170833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb22f44ce303b7331ea25c68f9cc24123cc7caa128b2bd1d0017a321eefab0a9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:41:48 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 19:41:48 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 19:41:48 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 19:41:49 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 19:41:49 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 19:41:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 19:45:31 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 19:45:32 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 19:45:32 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:45:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 19:45:32 GMT
USER varnish
# Thu, 23 Mar 2023 19:45:32 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 19:45:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7201f33e2e4539694a92607b61b1e2ea1a53f436c5855d96029b9db6cd82dba`  
		Last Modified: Thu, 23 Mar 2023 19:52:07 GMT  
		Size: 75.8 MB (75774064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db12df95277ae5ee27785ea05ef6bebee5a443b7747e7e56cfef27b7f85b0230`  
		Last Modified: Thu, 23 Mar 2023 19:51:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; ppc64le

```console
$ docker pull varnish@sha256:99a9dcf0cddca561abbcd5bc5b002adbb083de964d8746e3063cab564573c331
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106076410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e817121269101ae25eb3c824355809f156a4e72be8a908710817a5575d2fb848`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:43:55 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Wed, 12 Apr 2023 00:43:56 GMT
ARG VARNISH_VERSION=7.3.0
# Wed, 12 Apr 2023 00:43:56 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Wed, 12 Apr 2023 00:43:57 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 12 Apr 2023 00:43:57 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 12 Apr 2023 00:43:58 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 12 Apr 2023 00:43:58 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Wed, 12 Apr 2023 00:43:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Wed, 12 Apr 2023 00:43:59 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 12 Apr 2023 00:44:00 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Wed, 12 Apr 2023 00:44:00 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 Apr 2023 00:55:22 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 12 Apr 2023 00:55:26 GMT
WORKDIR /etc/varnish
# Wed, 12 Apr 2023 00:55:26 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:55:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 Apr 2023 00:55:28 GMT
USER varnish
# Wed, 12 Apr 2023 00:55:28 GMT
EXPOSE 80 8443
# Wed, 12 Apr 2023 00:55:29 GMT
CMD []
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a23cf789a1d6f1a8f615b2f894ff5d23dfc1871bec09bf4ddc25dfc2f51729`  
		Last Modified: Wed, 12 Apr 2023 01:17:31 GMT  
		Size: 70.8 MB (70783923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f561be54d7ea2acd53189c9a5ceccfe7bcc785342020b6d142e731caa7146a85`  
		Last Modified: Wed, 12 Apr 2023 01:17:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; s390x

```console
$ docker pull varnish@sha256:f748dab7db2aef4a89ab5fbba3270bb4b7b4a9d91769dd4a06b1dfeca1d57a22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87097616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dce21e8c45603a8701fccb74b85b9028709de3d15d63f820ea22a4dd38aea5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:04:15 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 07:04:15 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 07:04:15 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 07:04:15 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 07:04:16 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:04:16 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:04:16 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:06:51 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:06:53 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:06:53 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:06:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:06:53 GMT
USER varnish
# Thu, 23 Mar 2023 07:06:53 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:06:54 GMT
CMD []
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed1e81cb3f95f54447b5519e283bea6931614c96f3725aa0df9795d68af88a`  
		Last Modified: Thu, 23 Mar 2023 07:11:51 GMT  
		Size: 57.5 MB (57450304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c04293d87cc93048f858704fab4e5c64021a66e803dbcb97a23b838db4cca7`  
		Last Modified: Thu, 23 Mar 2023 07:11:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3-alpine`

```console
$ docker pull varnish@sha256:1bcc61baae22531bd59b4f66ac0559b261907ca095d5eccf350ffb64f658c813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.3-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:5d53f3cea335d15c3e518d4b4bd9ed6d9723e83a11cba3a0096e8dd81bb500a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59350414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8db36f71eea7cd47b1a6202cc8f6c57788e74b167c002c0f960e288cf7166e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:14:39 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 02:14:39 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 02:14:40 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 02:14:40 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 02:16:00 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 02:16:00 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 02:16:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 02:16:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 02:16:01 GMT
USER varnish
# Thu, 30 Mar 2023 02:16:01 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 02:16:01 GMT
CMD []
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ecd0ddb0fcb995ea02ce3c7936dcb1d915a193f322ca158d7dad0631ac18af`  
		Last Modified: Thu, 30 Mar 2023 02:18:01 GMT  
		Size: 56.5 MB (56523322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7869007cb383d86d06b6b514b6d46fc40ac581add12bbbf143f319ba7a8e7015`  
		Last Modified: Thu, 30 Mar 2023 02:17:54 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:17ebddf73589304daba01e60bdc7bdb5bd09c4ec3a101619994a8c4d77fe4198
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45109401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39e8bab4b3a15d6f7cb3d240b0f058d4044628947338dda3270ad223d1af8f4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:05:06 GMT
ADD file:0516b2e2d8a5c0a3e85e67a20375312bdc586a63094d779b9ac92517cf74a19d in / 
# Wed, 29 Mar 2023 18:05:06 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:10:33 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 00:10:33 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 00:10:34 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 00:10:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 00:10:34 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 00:10:34 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 00:10:34 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 00:11:55 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 00:11:55 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 00:11:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 00:11:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 00:11:55 GMT
USER varnish
# Thu, 30 Mar 2023 00:11:55 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 00:11:55 GMT
CMD []
```

-	Layers:
	-	`sha256:fafb00bc68cf26e4a27ad2dce7303945ba9e40994e77c9269e610e0452ae9dce`  
		Last Modified: Wed, 29 Mar 2023 18:07:17 GMT  
		Size: 2.4 MB (2437606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f196af073038a0d6be5e1af91b28163c0eaca95c0243eac019991add8bb276`  
		Last Modified: Sat, 08 Apr 2023 02:40:45 GMT  
		Size: 42.7 MB (42671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d483681d593a3936990d940c17cfe78497a6b081463653220e180980f80af780`  
		Last Modified: Sat, 08 Apr 2023 02:40:39 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cdef2ee791f1fea0bb632e5fdbe7ab3d1dc08640e869ecbaad970af72cb62ed2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52090155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26631d7414d095798d5e7800471d90767915486d8223cffd0d9a95dc9379d7a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:53:56 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 05:53:57 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 05:53:57 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 05:53:57 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 05:55:07 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 05:55:07 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 05:55:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 05:55:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 05:55:07 GMT
USER varnish
# Thu, 30 Mar 2023 05:55:07 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 05:55:07 GMT
CMD []
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50d982964542b8110c8924003584227b1310249ecd04ddd79df743a575bc925`  
		Last Modified: Thu, 30 Mar 2023 05:56:46 GMT  
		Size: 49.4 MB (49367657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12b6ca5add2e0d079fd385cac5fdbaa5864540dcd10b770e1548f117a90bd41`  
		Last Modified: Thu, 30 Mar 2023 05:56:40 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; 386

```console
$ docker pull varnish@sha256:f834ae921c56c3eb925d9bea6bc8e1ab80f60425be23ff96bb15cdba11930285
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59538735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec87c585f44b8fefde94e4cb6f1eef3835e1db4c9686969169c7cd5dd6fb735`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:33:46 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 01:33:46 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 01:33:46 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 01:33:47 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 01:33:47 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 01:33:47 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 01:35:56 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 01:35:56 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 01:35:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 01:35:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 01:35:56 GMT
USER varnish
# Thu, 30 Mar 2023 01:35:56 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 01:35:57 GMT
CMD []
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da4d176e921bbb51748136a8fbf517d3cc60798e35724aebdd51ecf2b61ab6`  
		Last Modified: Thu, 30 Mar 2023 01:38:40 GMT  
		Size: 56.7 MB (56705662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a78548a60d6b9d7baf75051feb0fca2994834030bbc04a3645a4572a9757471`  
		Last Modified: Thu, 30 Mar 2023 01:38:30 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:909478b58a275ec2ab8a14120cc9591ebbbdff86f860ea8df1485ae2c264e488
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49136000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d067fd63b0dd3bfee0cefb4eaba611ad41e8cfecb8b2c16ada69e7e227fcb7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:16:40 GMT
ADD file:3c2a8d553fa0998f13f86592f104a9a4ad14f8db46dfa9145c8fbbca0b87ee9a in / 
# Wed, 29 Mar 2023 18:16:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:33:21 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 04:33:22 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 04:33:22 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 04:33:22 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 04:33:24 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 04:33:24 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 04:33:24 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 04:35:35 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 04:35:37 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 04:35:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 04:35:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 04:35:38 GMT
USER varnish
# Thu, 30 Mar 2023 04:35:38 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 04:35:38 GMT
CMD []
```

-	Layers:
	-	`sha256:0b40b0bd0da3095d93bf74233a1d0bf638b2511fee461df8f6a71aad5a038589`  
		Last Modified: Wed, 29 Mar 2023 18:17:38 GMT  
		Size: 2.8 MB (2813760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5980c95097dfced199688de3f6aa45cd2216bfddef048561966b6608945af2f0`  
		Last Modified: Thu, 30 Mar 2023 04:38:24 GMT  
		Size: 46.3 MB (46321744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690ae6fe9c6e1be629171f54ae05b866b6572efa3b1d22692d741929e7d11bb7`  
		Last Modified: Thu, 30 Mar 2023 04:38:12 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:2fabb6c5fa95ead9711c9785ebab43a38eacb02b418775d6b5ab1a73fa8acc8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47598984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb61c9640b3da92089de86d78ac057c997e5d877f757120cda472c896b941e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:42:07 GMT
ADD file:5cf392863cd9a0735de88f9e7dab93c9e74aca59ca05b792943cf3b621ea2c59 in / 
# Wed, 29 Mar 2023 17:42:07 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 23:08:14 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_VERSION=7.3.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Wed, 29 Mar 2023 23:08:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Wed, 29 Mar 2023 23:08:15 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 29 Mar 2023 23:08:15 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Wed, 29 Mar 2023 23:08:15 GMT
ENV VARNISH_SIZE=100M
# Wed, 29 Mar 2023 23:09:46 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Wed, 29 Mar 2023 23:09:47 GMT
WORKDIR /etc/varnish
# Wed, 29 Mar 2023 23:09:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 29 Mar 2023 23:09:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 29 Mar 2023 23:09:48 GMT
USER varnish
# Wed, 29 Mar 2023 23:09:48 GMT
EXPOSE 80 8443
# Wed, 29 Mar 2023 23:09:48 GMT
CMD []
```

-	Layers:
	-	`sha256:1536575ac9c5f5fff4522c60d4610af0a52be584c36e652080c6c0ad169d4f27`  
		Last Modified: Wed, 29 Mar 2023 17:42:42 GMT  
		Size: 2.6 MB (2610636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadb2417c7920374afa7798d98c70d2f0a8290f641bb3dbc112a2158ac097a2d`  
		Last Modified: Wed, 29 Mar 2023 23:12:02 GMT  
		Size: 45.0 MB (44987850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a556b2e0ae2040be8338c713604078ac74fa7ec335f48fff28337d8b007e52`  
		Last Modified: Wed, 29 Mar 2023 23:11:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3.0`

```console
$ docker pull varnish@sha256:2f211fd175cf8d3b2803abe0bcc1b42a94c2557568e4f301340f18c517254acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.3.0` - linux; amd64

```console
$ docker pull varnish@sha256:966e57e0f907166e5cfe74f03c70027a7bfeb7763d21ef6c0421f62415e9cde0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106798860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde7e0fae0241ca1def63efb79171503518a8488438150538534de27d6aa8e8e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:35:42 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 08:35:43 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 08:35:43 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 08:35:43 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 08:38:51 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 08:38:52 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 08:38:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 08:38:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 08:38:52 GMT
USER varnish
# Thu, 23 Mar 2023 08:38:52 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 08:38:52 GMT
CMD []
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ebc78fcc0bfd5f9a86a59c7ba9dc92d6c6ac286ed8792d8616139b3f728557`  
		Last Modified: Thu, 23 Mar 2023 08:44:29 GMT  
		Size: 75.4 MB (75386965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3679bcba66926e3e08e43f6a3b27ae9c5902dca3a35c8a3b5c4da60d413ff28d`  
		Last Modified: Thu, 23 Mar 2023 08:44:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e853c6bce2a44d87519a8074817ef212fab243e6dd356a4abd7e512d7067617c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83146210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad755a8b29b5be4bc688f975df90490adc469fb52f225c1498c7796c7647faf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:27:26 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 12:27:26 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 12:27:26 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 12:27:27 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 12:30:37 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 12:30:37 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 12:30:38 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:30:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 12:30:38 GMT
USER varnish
# Thu, 23 Mar 2023 12:30:38 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 12:30:38 GMT
CMD []
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e2d8b662d5f484247a6608121d266efd1a66ababf38e85884f4b25c943a1b`  
		Last Modified: Thu, 23 Mar 2023 12:36:07 GMT  
		Size: 56.6 MB (56568388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e95c1272c5b14b209ef35f4b8e7b15c931bf708123d990755924aa025813cc`  
		Last Modified: Thu, 23 Mar 2023 12:36:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e5c5ffd6dc2c95d7fee3e5bcbf2d300bb9b0f33918460846e02bb0bc789617c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100588684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720135e26f679dcaa1eeddcd6ae73bb0c8c9cda47e9f248bc72656427f8d3bb5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:25:32 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 07:25:32 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 07:25:33 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:25:33 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:25:33 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:28:40 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:28:40 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:28:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:28:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:28:40 GMT
USER varnish
# Thu, 23 Mar 2023 07:28:40 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:28:41 GMT
CMD []
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88629f01162d8c785683ae0fbde30f240c471df8fb8aad45c270bea1517206`  
		Last Modified: Thu, 23 Mar 2023 07:33:28 GMT  
		Size: 70.5 MB (70525493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132c73bad44c61b38ee1ac99c3b7cbcedeb6aaf28804afc1b2f5e9cc4240a43`  
		Last Modified: Thu, 23 Mar 2023 07:33:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.0` - linux; 386

```console
$ docker pull varnish@sha256:d419b0f75d76108ac53df1fb2fe379af01c91466546b17a14308403e11c46a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108170833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb22f44ce303b7331ea25c68f9cc24123cc7caa128b2bd1d0017a321eefab0a9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:41:48 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 19:41:48 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 19:41:48 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 19:41:49 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 19:41:49 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 19:41:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 19:45:31 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 19:45:32 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 19:45:32 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:45:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 19:45:32 GMT
USER varnish
# Thu, 23 Mar 2023 19:45:32 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 19:45:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7201f33e2e4539694a92607b61b1e2ea1a53f436c5855d96029b9db6cd82dba`  
		Last Modified: Thu, 23 Mar 2023 19:52:07 GMT  
		Size: 75.8 MB (75774064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db12df95277ae5ee27785ea05ef6bebee5a443b7747e7e56cfef27b7f85b0230`  
		Last Modified: Thu, 23 Mar 2023 19:51:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:99a9dcf0cddca561abbcd5bc5b002adbb083de964d8746e3063cab564573c331
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106076410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e817121269101ae25eb3c824355809f156a4e72be8a908710817a5575d2fb848`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:43:55 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Wed, 12 Apr 2023 00:43:56 GMT
ARG VARNISH_VERSION=7.3.0
# Wed, 12 Apr 2023 00:43:56 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Wed, 12 Apr 2023 00:43:57 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 12 Apr 2023 00:43:57 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 12 Apr 2023 00:43:58 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 12 Apr 2023 00:43:58 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Wed, 12 Apr 2023 00:43:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Wed, 12 Apr 2023 00:43:59 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 12 Apr 2023 00:44:00 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Wed, 12 Apr 2023 00:44:00 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 Apr 2023 00:55:22 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 12 Apr 2023 00:55:26 GMT
WORKDIR /etc/varnish
# Wed, 12 Apr 2023 00:55:26 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:55:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 Apr 2023 00:55:28 GMT
USER varnish
# Wed, 12 Apr 2023 00:55:28 GMT
EXPOSE 80 8443
# Wed, 12 Apr 2023 00:55:29 GMT
CMD []
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a23cf789a1d6f1a8f615b2f894ff5d23dfc1871bec09bf4ddc25dfc2f51729`  
		Last Modified: Wed, 12 Apr 2023 01:17:31 GMT  
		Size: 70.8 MB (70783923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f561be54d7ea2acd53189c9a5ceccfe7bcc785342020b6d142e731caa7146a85`  
		Last Modified: Wed, 12 Apr 2023 01:17:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.0` - linux; s390x

```console
$ docker pull varnish@sha256:f748dab7db2aef4a89ab5fbba3270bb4b7b4a9d91769dd4a06b1dfeca1d57a22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87097616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dce21e8c45603a8701fccb74b85b9028709de3d15d63f820ea22a4dd38aea5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:04:15 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 07:04:15 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 07:04:15 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 07:04:15 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 07:04:16 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:04:16 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:04:16 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:06:51 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:06:53 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:06:53 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:06:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:06:53 GMT
USER varnish
# Thu, 23 Mar 2023 07:06:53 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:06:54 GMT
CMD []
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed1e81cb3f95f54447b5519e283bea6931614c96f3725aa0df9795d68af88a`  
		Last Modified: Thu, 23 Mar 2023 07:11:51 GMT  
		Size: 57.5 MB (57450304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c04293d87cc93048f858704fab4e5c64021a66e803dbcb97a23b838db4cca7`  
		Last Modified: Thu, 23 Mar 2023 07:11:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3.0-alpine`

```console
$ docker pull varnish@sha256:1bcc61baae22531bd59b4f66ac0559b261907ca095d5eccf350ffb64f658c813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.3.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:5d53f3cea335d15c3e518d4b4bd9ed6d9723e83a11cba3a0096e8dd81bb500a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59350414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8db36f71eea7cd47b1a6202cc8f6c57788e74b167c002c0f960e288cf7166e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:14:39 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 02:14:39 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 02:14:40 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 02:14:40 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 02:16:00 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 02:16:00 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 02:16:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 02:16:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 02:16:01 GMT
USER varnish
# Thu, 30 Mar 2023 02:16:01 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 02:16:01 GMT
CMD []
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ecd0ddb0fcb995ea02ce3c7936dcb1d915a193f322ca158d7dad0631ac18af`  
		Last Modified: Thu, 30 Mar 2023 02:18:01 GMT  
		Size: 56.5 MB (56523322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7869007cb383d86d06b6b514b6d46fc40ac581add12bbbf143f319ba7a8e7015`  
		Last Modified: Thu, 30 Mar 2023 02:17:54 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:17ebddf73589304daba01e60bdc7bdb5bd09c4ec3a101619994a8c4d77fe4198
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45109401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39e8bab4b3a15d6f7cb3d240b0f058d4044628947338dda3270ad223d1af8f4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:05:06 GMT
ADD file:0516b2e2d8a5c0a3e85e67a20375312bdc586a63094d779b9ac92517cf74a19d in / 
# Wed, 29 Mar 2023 18:05:06 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:10:33 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 00:10:33 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 00:10:34 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 00:10:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 00:10:34 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 00:10:34 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 00:10:34 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 00:11:55 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 00:11:55 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 00:11:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 00:11:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 00:11:55 GMT
USER varnish
# Thu, 30 Mar 2023 00:11:55 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 00:11:55 GMT
CMD []
```

-	Layers:
	-	`sha256:fafb00bc68cf26e4a27ad2dce7303945ba9e40994e77c9269e610e0452ae9dce`  
		Last Modified: Wed, 29 Mar 2023 18:07:17 GMT  
		Size: 2.4 MB (2437606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f196af073038a0d6be5e1af91b28163c0eaca95c0243eac019991add8bb276`  
		Last Modified: Sat, 08 Apr 2023 02:40:45 GMT  
		Size: 42.7 MB (42671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d483681d593a3936990d940c17cfe78497a6b081463653220e180980f80af780`  
		Last Modified: Sat, 08 Apr 2023 02:40:39 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cdef2ee791f1fea0bb632e5fdbe7ab3d1dc08640e869ecbaad970af72cb62ed2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52090155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26631d7414d095798d5e7800471d90767915486d8223cffd0d9a95dc9379d7a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:53:56 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 05:53:57 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 05:53:57 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 05:53:57 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 05:55:07 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 05:55:07 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 05:55:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 05:55:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 05:55:07 GMT
USER varnish
# Thu, 30 Mar 2023 05:55:07 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 05:55:07 GMT
CMD []
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50d982964542b8110c8924003584227b1310249ecd04ddd79df743a575bc925`  
		Last Modified: Thu, 30 Mar 2023 05:56:46 GMT  
		Size: 49.4 MB (49367657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12b6ca5add2e0d079fd385cac5fdbaa5864540dcd10b770e1548f117a90bd41`  
		Last Modified: Thu, 30 Mar 2023 05:56:40 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:f834ae921c56c3eb925d9bea6bc8e1ab80f60425be23ff96bb15cdba11930285
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59538735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec87c585f44b8fefde94e4cb6f1eef3835e1db4c9686969169c7cd5dd6fb735`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:33:46 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 01:33:46 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 01:33:46 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 01:33:47 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 01:33:47 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 01:33:47 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 01:35:56 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 01:35:56 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 01:35:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 01:35:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 01:35:56 GMT
USER varnish
# Thu, 30 Mar 2023 01:35:56 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 01:35:57 GMT
CMD []
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da4d176e921bbb51748136a8fbf517d3cc60798e35724aebdd51ecf2b61ab6`  
		Last Modified: Thu, 30 Mar 2023 01:38:40 GMT  
		Size: 56.7 MB (56705662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a78548a60d6b9d7baf75051feb0fca2994834030bbc04a3645a4572a9757471`  
		Last Modified: Thu, 30 Mar 2023 01:38:30 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:909478b58a275ec2ab8a14120cc9591ebbbdff86f860ea8df1485ae2c264e488
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49136000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d067fd63b0dd3bfee0cefb4eaba611ad41e8cfecb8b2c16ada69e7e227fcb7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:16:40 GMT
ADD file:3c2a8d553fa0998f13f86592f104a9a4ad14f8db46dfa9145c8fbbca0b87ee9a in / 
# Wed, 29 Mar 2023 18:16:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:33:21 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 04:33:22 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 04:33:22 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 04:33:22 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 04:33:24 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 04:33:24 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 04:33:24 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 04:35:35 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 04:35:37 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 04:35:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 04:35:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 04:35:38 GMT
USER varnish
# Thu, 30 Mar 2023 04:35:38 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 04:35:38 GMT
CMD []
```

-	Layers:
	-	`sha256:0b40b0bd0da3095d93bf74233a1d0bf638b2511fee461df8f6a71aad5a038589`  
		Last Modified: Wed, 29 Mar 2023 18:17:38 GMT  
		Size: 2.8 MB (2813760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5980c95097dfced199688de3f6aa45cd2216bfddef048561966b6608945af2f0`  
		Last Modified: Thu, 30 Mar 2023 04:38:24 GMT  
		Size: 46.3 MB (46321744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690ae6fe9c6e1be629171f54ae05b866b6572efa3b1d22692d741929e7d11bb7`  
		Last Modified: Thu, 30 Mar 2023 04:38:12 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:2fabb6c5fa95ead9711c9785ebab43a38eacb02b418775d6b5ab1a73fa8acc8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47598984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb61c9640b3da92089de86d78ac057c997e5d877f757120cda472c896b941e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:42:07 GMT
ADD file:5cf392863cd9a0735de88f9e7dab93c9e74aca59ca05b792943cf3b621ea2c59 in / 
# Wed, 29 Mar 2023 17:42:07 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 23:08:14 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_VERSION=7.3.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Wed, 29 Mar 2023 23:08:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Wed, 29 Mar 2023 23:08:15 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 29 Mar 2023 23:08:15 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Wed, 29 Mar 2023 23:08:15 GMT
ENV VARNISH_SIZE=100M
# Wed, 29 Mar 2023 23:09:46 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Wed, 29 Mar 2023 23:09:47 GMT
WORKDIR /etc/varnish
# Wed, 29 Mar 2023 23:09:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 29 Mar 2023 23:09:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 29 Mar 2023 23:09:48 GMT
USER varnish
# Wed, 29 Mar 2023 23:09:48 GMT
EXPOSE 80 8443
# Wed, 29 Mar 2023 23:09:48 GMT
CMD []
```

-	Layers:
	-	`sha256:1536575ac9c5f5fff4522c60d4610af0a52be584c36e652080c6c0ad169d4f27`  
		Last Modified: Wed, 29 Mar 2023 17:42:42 GMT  
		Size: 2.6 MB (2610636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadb2417c7920374afa7798d98c70d2f0a8290f641bb3dbc112a2158ac097a2d`  
		Last Modified: Wed, 29 Mar 2023 23:12:02 GMT  
		Size: 45.0 MB (44987850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a556b2e0ae2040be8338c713604078ac74fa7ec335f48fff28337d8b007e52`  
		Last Modified: Wed, 29 Mar 2023 23:11:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:alpine`

```console
$ docker pull varnish@sha256:1bcc61baae22531bd59b4f66ac0559b261907ca095d5eccf350ffb64f658c813
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
$ docker pull varnish@sha256:5d53f3cea335d15c3e518d4b4bd9ed6d9723e83a11cba3a0096e8dd81bb500a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59350414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8db36f71eea7cd47b1a6202cc8f6c57788e74b167c002c0f960e288cf7166e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:14:39 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 02:14:39 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 02:14:40 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 02:14:40 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 02:16:00 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 02:16:00 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 02:16:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 02:16:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 02:16:01 GMT
USER varnish
# Thu, 30 Mar 2023 02:16:01 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 02:16:01 GMT
CMD []
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ecd0ddb0fcb995ea02ce3c7936dcb1d915a193f322ca158d7dad0631ac18af`  
		Last Modified: Thu, 30 Mar 2023 02:18:01 GMT  
		Size: 56.5 MB (56523322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7869007cb383d86d06b6b514b6d46fc40ac581add12bbbf143f319ba7a8e7015`  
		Last Modified: Thu, 30 Mar 2023 02:17:54 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:17ebddf73589304daba01e60bdc7bdb5bd09c4ec3a101619994a8c4d77fe4198
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45109401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39e8bab4b3a15d6f7cb3d240b0f058d4044628947338dda3270ad223d1af8f4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:05:06 GMT
ADD file:0516b2e2d8a5c0a3e85e67a20375312bdc586a63094d779b9ac92517cf74a19d in / 
# Wed, 29 Mar 2023 18:05:06 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:10:33 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 00:10:33 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 00:10:34 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 00:10:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 00:10:34 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 00:10:34 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 00:10:34 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 00:11:55 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 00:11:55 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 00:11:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 00:11:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 00:11:55 GMT
USER varnish
# Thu, 30 Mar 2023 00:11:55 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 00:11:55 GMT
CMD []
```

-	Layers:
	-	`sha256:fafb00bc68cf26e4a27ad2dce7303945ba9e40994e77c9269e610e0452ae9dce`  
		Last Modified: Wed, 29 Mar 2023 18:07:17 GMT  
		Size: 2.4 MB (2437606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f196af073038a0d6be5e1af91b28163c0eaca95c0243eac019991add8bb276`  
		Last Modified: Sat, 08 Apr 2023 02:40:45 GMT  
		Size: 42.7 MB (42671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d483681d593a3936990d940c17cfe78497a6b081463653220e180980f80af780`  
		Last Modified: Sat, 08 Apr 2023 02:40:39 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cdef2ee791f1fea0bb632e5fdbe7ab3d1dc08640e869ecbaad970af72cb62ed2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52090155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26631d7414d095798d5e7800471d90767915486d8223cffd0d9a95dc9379d7a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:53:56 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 05:53:57 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 05:53:57 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 05:53:57 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 05:55:07 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 05:55:07 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 05:55:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 05:55:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 05:55:07 GMT
USER varnish
# Thu, 30 Mar 2023 05:55:07 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 05:55:07 GMT
CMD []
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50d982964542b8110c8924003584227b1310249ecd04ddd79df743a575bc925`  
		Last Modified: Thu, 30 Mar 2023 05:56:46 GMT  
		Size: 49.4 MB (49367657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12b6ca5add2e0d079fd385cac5fdbaa5864540dcd10b770e1548f117a90bd41`  
		Last Modified: Thu, 30 Mar 2023 05:56:40 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:f834ae921c56c3eb925d9bea6bc8e1ab80f60425be23ff96bb15cdba11930285
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59538735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec87c585f44b8fefde94e4cb6f1eef3835e1db4c9686969169c7cd5dd6fb735`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:33:46 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 01:33:46 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 01:33:46 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 01:33:47 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 01:33:47 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 01:33:47 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 01:35:56 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 01:35:56 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 01:35:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 01:35:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 01:35:56 GMT
USER varnish
# Thu, 30 Mar 2023 01:35:56 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 01:35:57 GMT
CMD []
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da4d176e921bbb51748136a8fbf517d3cc60798e35724aebdd51ecf2b61ab6`  
		Last Modified: Thu, 30 Mar 2023 01:38:40 GMT  
		Size: 56.7 MB (56705662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a78548a60d6b9d7baf75051feb0fca2994834030bbc04a3645a4572a9757471`  
		Last Modified: Thu, 30 Mar 2023 01:38:30 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:909478b58a275ec2ab8a14120cc9591ebbbdff86f860ea8df1485ae2c264e488
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49136000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d067fd63b0dd3bfee0cefb4eaba611ad41e8cfecb8b2c16ada69e7e227fcb7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:16:40 GMT
ADD file:3c2a8d553fa0998f13f86592f104a9a4ad14f8db46dfa9145c8fbbca0b87ee9a in / 
# Wed, 29 Mar 2023 18:16:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:33:21 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 04:33:22 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 04:33:22 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 04:33:22 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 04:33:24 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 04:33:24 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 04:33:24 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 04:35:35 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 04:35:37 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 04:35:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 04:35:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 04:35:38 GMT
USER varnish
# Thu, 30 Mar 2023 04:35:38 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 04:35:38 GMT
CMD []
```

-	Layers:
	-	`sha256:0b40b0bd0da3095d93bf74233a1d0bf638b2511fee461df8f6a71aad5a038589`  
		Last Modified: Wed, 29 Mar 2023 18:17:38 GMT  
		Size: 2.8 MB (2813760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5980c95097dfced199688de3f6aa45cd2216bfddef048561966b6608945af2f0`  
		Last Modified: Thu, 30 Mar 2023 04:38:24 GMT  
		Size: 46.3 MB (46321744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690ae6fe9c6e1be629171f54ae05b866b6572efa3b1d22692d741929e7d11bb7`  
		Last Modified: Thu, 30 Mar 2023 04:38:12 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:2fabb6c5fa95ead9711c9785ebab43a38eacb02b418775d6b5ab1a73fa8acc8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47598984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb61c9640b3da92089de86d78ac057c997e5d877f757120cda472c896b941e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:42:07 GMT
ADD file:5cf392863cd9a0735de88f9e7dab93c9e74aca59ca05b792943cf3b621ea2c59 in / 
# Wed, 29 Mar 2023 17:42:07 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 23:08:14 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_VERSION=7.3.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Wed, 29 Mar 2023 23:08:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Wed, 29 Mar 2023 23:08:15 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 29 Mar 2023 23:08:15 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Wed, 29 Mar 2023 23:08:15 GMT
ENV VARNISH_SIZE=100M
# Wed, 29 Mar 2023 23:09:46 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Wed, 29 Mar 2023 23:09:47 GMT
WORKDIR /etc/varnish
# Wed, 29 Mar 2023 23:09:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 29 Mar 2023 23:09:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 29 Mar 2023 23:09:48 GMT
USER varnish
# Wed, 29 Mar 2023 23:09:48 GMT
EXPOSE 80 8443
# Wed, 29 Mar 2023 23:09:48 GMT
CMD []
```

-	Layers:
	-	`sha256:1536575ac9c5f5fff4522c60d4610af0a52be584c36e652080c6c0ad169d4f27`  
		Last Modified: Wed, 29 Mar 2023 17:42:42 GMT  
		Size: 2.6 MB (2610636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadb2417c7920374afa7798d98c70d2f0a8290f641bb3dbc112a2158ac097a2d`  
		Last Modified: Wed, 29 Mar 2023 23:12:02 GMT  
		Size: 45.0 MB (44987850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a556b2e0ae2040be8338c713604078ac74fa7ec335f48fff28337d8b007e52`  
		Last Modified: Wed, 29 Mar 2023 23:11:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:2f211fd175cf8d3b2803abe0bcc1b42a94c2557568e4f301340f18c517254acb
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
$ docker pull varnish@sha256:966e57e0f907166e5cfe74f03c70027a7bfeb7763d21ef6c0421f62415e9cde0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106798860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde7e0fae0241ca1def63efb79171503518a8488438150538534de27d6aa8e8e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:35:42 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 08:35:43 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 08:35:43 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 08:35:43 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 08:38:51 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 08:38:52 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 08:38:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 08:38:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 08:38:52 GMT
USER varnish
# Thu, 23 Mar 2023 08:38:52 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 08:38:52 GMT
CMD []
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ebc78fcc0bfd5f9a86a59c7ba9dc92d6c6ac286ed8792d8616139b3f728557`  
		Last Modified: Thu, 23 Mar 2023 08:44:29 GMT  
		Size: 75.4 MB (75386965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3679bcba66926e3e08e43f6a3b27ae9c5902dca3a35c8a3b5c4da60d413ff28d`  
		Last Modified: Thu, 23 Mar 2023 08:44:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e853c6bce2a44d87519a8074817ef212fab243e6dd356a4abd7e512d7067617c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83146210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad755a8b29b5be4bc688f975df90490adc469fb52f225c1498c7796c7647faf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:27:26 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 12:27:26 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 12:27:26 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 12:27:27 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 12:30:37 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 12:30:37 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 12:30:38 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:30:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 12:30:38 GMT
USER varnish
# Thu, 23 Mar 2023 12:30:38 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 12:30:38 GMT
CMD []
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e2d8b662d5f484247a6608121d266efd1a66ababf38e85884f4b25c943a1b`  
		Last Modified: Thu, 23 Mar 2023 12:36:07 GMT  
		Size: 56.6 MB (56568388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e95c1272c5b14b209ef35f4b8e7b15c931bf708123d990755924aa025813cc`  
		Last Modified: Thu, 23 Mar 2023 12:36:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e5c5ffd6dc2c95d7fee3e5bcbf2d300bb9b0f33918460846e02bb0bc789617c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100588684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720135e26f679dcaa1eeddcd6ae73bb0c8c9cda47e9f248bc72656427f8d3bb5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:25:32 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 07:25:32 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 07:25:33 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:25:33 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:25:33 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:28:40 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:28:40 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:28:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:28:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:28:40 GMT
USER varnish
# Thu, 23 Mar 2023 07:28:40 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:28:41 GMT
CMD []
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88629f01162d8c785683ae0fbde30f240c471df8fb8aad45c270bea1517206`  
		Last Modified: Thu, 23 Mar 2023 07:33:28 GMT  
		Size: 70.5 MB (70525493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132c73bad44c61b38ee1ac99c3b7cbcedeb6aaf28804afc1b2f5e9cc4240a43`  
		Last Modified: Thu, 23 Mar 2023 07:33:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:d419b0f75d76108ac53df1fb2fe379af01c91466546b17a14308403e11c46a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108170833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb22f44ce303b7331ea25c68f9cc24123cc7caa128b2bd1d0017a321eefab0a9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:41:48 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 19:41:48 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 19:41:48 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 19:41:49 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 19:41:49 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 19:41:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 19:45:31 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 19:45:32 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 19:45:32 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:45:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 19:45:32 GMT
USER varnish
# Thu, 23 Mar 2023 19:45:32 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 19:45:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7201f33e2e4539694a92607b61b1e2ea1a53f436c5855d96029b9db6cd82dba`  
		Last Modified: Thu, 23 Mar 2023 19:52:07 GMT  
		Size: 75.8 MB (75774064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db12df95277ae5ee27785ea05ef6bebee5a443b7747e7e56cfef27b7f85b0230`  
		Last Modified: Thu, 23 Mar 2023 19:51:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:99a9dcf0cddca561abbcd5bc5b002adbb083de964d8746e3063cab564573c331
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106076410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e817121269101ae25eb3c824355809f156a4e72be8a908710817a5575d2fb848`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:43:55 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Wed, 12 Apr 2023 00:43:56 GMT
ARG VARNISH_VERSION=7.3.0
# Wed, 12 Apr 2023 00:43:56 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Wed, 12 Apr 2023 00:43:57 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 12 Apr 2023 00:43:57 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 12 Apr 2023 00:43:58 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 12 Apr 2023 00:43:58 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Wed, 12 Apr 2023 00:43:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Wed, 12 Apr 2023 00:43:59 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 12 Apr 2023 00:44:00 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Wed, 12 Apr 2023 00:44:00 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 Apr 2023 00:55:22 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 12 Apr 2023 00:55:26 GMT
WORKDIR /etc/varnish
# Wed, 12 Apr 2023 00:55:26 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:55:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 Apr 2023 00:55:28 GMT
USER varnish
# Wed, 12 Apr 2023 00:55:28 GMT
EXPOSE 80 8443
# Wed, 12 Apr 2023 00:55:29 GMT
CMD []
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a23cf789a1d6f1a8f615b2f894ff5d23dfc1871bec09bf4ddc25dfc2f51729`  
		Last Modified: Wed, 12 Apr 2023 01:17:31 GMT  
		Size: 70.8 MB (70783923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f561be54d7ea2acd53189c9a5ceccfe7bcc785342020b6d142e731caa7146a85`  
		Last Modified: Wed, 12 Apr 2023 01:17:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:f748dab7db2aef4a89ab5fbba3270bb4b7b4a9d91769dd4a06b1dfeca1d57a22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87097616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dce21e8c45603a8701fccb74b85b9028709de3d15d63f820ea22a4dd38aea5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:04:15 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 07:04:15 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 07:04:15 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 07:04:15 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 07:04:16 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:04:16 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:04:16 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:06:51 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:06:53 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:06:53 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:06:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:06:53 GMT
USER varnish
# Thu, 23 Mar 2023 07:06:53 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:06:54 GMT
CMD []
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed1e81cb3f95f54447b5519e283bea6931614c96f3725aa0df9795d68af88a`  
		Last Modified: Thu, 23 Mar 2023 07:11:51 GMT  
		Size: 57.5 MB (57450304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c04293d87cc93048f858704fab4e5c64021a66e803dbcb97a23b838db4cca7`  
		Last Modified: Thu, 23 Mar 2023 07:11:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:1bcc61baae22531bd59b4f66ac0559b261907ca095d5eccf350ffb64f658c813
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
$ docker pull varnish@sha256:5d53f3cea335d15c3e518d4b4bd9ed6d9723e83a11cba3a0096e8dd81bb500a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59350414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8db36f71eea7cd47b1a6202cc8f6c57788e74b167c002c0f960e288cf7166e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:14:39 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 02:14:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 02:14:39 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 02:14:40 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 02:14:40 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 02:16:00 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 02:16:00 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 02:16:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 02:16:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 02:16:01 GMT
USER varnish
# Thu, 30 Mar 2023 02:16:01 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 02:16:01 GMT
CMD []
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ecd0ddb0fcb995ea02ce3c7936dcb1d915a193f322ca158d7dad0631ac18af`  
		Last Modified: Thu, 30 Mar 2023 02:18:01 GMT  
		Size: 56.5 MB (56523322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7869007cb383d86d06b6b514b6d46fc40ac581add12bbbf143f319ba7a8e7015`  
		Last Modified: Thu, 30 Mar 2023 02:17:54 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:17ebddf73589304daba01e60bdc7bdb5bd09c4ec3a101619994a8c4d77fe4198
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45109401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39e8bab4b3a15d6f7cb3d240b0f058d4044628947338dda3270ad223d1af8f4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:05:06 GMT
ADD file:0516b2e2d8a5c0a3e85e67a20375312bdc586a63094d779b9ac92517cf74a19d in / 
# Wed, 29 Mar 2023 18:05:06 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:10:33 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 00:10:33 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 00:10:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 00:10:34 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 00:10:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 00:10:34 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 00:10:34 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 00:10:34 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 00:11:55 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 00:11:55 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 00:11:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 00:11:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 00:11:55 GMT
USER varnish
# Thu, 30 Mar 2023 00:11:55 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 00:11:55 GMT
CMD []
```

-	Layers:
	-	`sha256:fafb00bc68cf26e4a27ad2dce7303945ba9e40994e77c9269e610e0452ae9dce`  
		Last Modified: Wed, 29 Mar 2023 18:07:17 GMT  
		Size: 2.4 MB (2437606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f196af073038a0d6be5e1af91b28163c0eaca95c0243eac019991add8bb276`  
		Last Modified: Sat, 08 Apr 2023 02:40:45 GMT  
		Size: 42.7 MB (42671302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d483681d593a3936990d940c17cfe78497a6b081463653220e180980f80af780`  
		Last Modified: Sat, 08 Apr 2023 02:40:39 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cdef2ee791f1fea0bb632e5fdbe7ab3d1dc08640e869ecbaad970af72cb62ed2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52090155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26631d7414d095798d5e7800471d90767915486d8223cffd0d9a95dc9379d7a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:53:56 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 05:53:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 05:53:57 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 05:53:57 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 05:53:57 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 05:55:07 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 05:55:07 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 05:55:07 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 05:55:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 05:55:07 GMT
USER varnish
# Thu, 30 Mar 2023 05:55:07 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 05:55:07 GMT
CMD []
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50d982964542b8110c8924003584227b1310249ecd04ddd79df743a575bc925`  
		Last Modified: Thu, 30 Mar 2023 05:56:46 GMT  
		Size: 49.4 MB (49367657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12b6ca5add2e0d079fd385cac5fdbaa5864540dcd10b770e1548f117a90bd41`  
		Last Modified: Thu, 30 Mar 2023 05:56:40 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:f834ae921c56c3eb925d9bea6bc8e1ab80f60425be23ff96bb15cdba11930285
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59538735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec87c585f44b8fefde94e4cb6f1eef3835e1db4c9686969169c7cd5dd6fb735`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:33:46 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 01:33:46 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 01:33:46 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 01:33:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 01:33:47 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 01:33:47 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 01:33:47 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 01:35:56 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 01:35:56 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 01:35:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 01:35:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 01:35:56 GMT
USER varnish
# Thu, 30 Mar 2023 01:35:56 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 01:35:57 GMT
CMD []
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da4d176e921bbb51748136a8fbf517d3cc60798e35724aebdd51ecf2b61ab6`  
		Last Modified: Thu, 30 Mar 2023 01:38:40 GMT  
		Size: 56.7 MB (56705662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a78548a60d6b9d7baf75051feb0fca2994834030bbc04a3645a4572a9757471`  
		Last Modified: Thu, 30 Mar 2023 01:38:30 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:909478b58a275ec2ab8a14120cc9591ebbbdff86f860ea8df1485ae2c264e488
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49136000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d067fd63b0dd3bfee0cefb4eaba611ad41e8cfecb8b2c16ada69e7e227fcb7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:16:40 GMT
ADD file:3c2a8d553fa0998f13f86592f104a9a4ad14f8db46dfa9145c8fbbca0b87ee9a in / 
# Wed, 29 Mar 2023 18:16:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:33:21 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 30 Mar 2023 04:33:22 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 30 Mar 2023 04:33:22 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 30 Mar 2023 04:33:22 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 30 Mar 2023 04:33:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 30 Mar 2023 04:33:24 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 04:33:24 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 04:33:24 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 04:35:35 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 04:35:37 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 04:35:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 04:35:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 04:35:38 GMT
USER varnish
# Thu, 30 Mar 2023 04:35:38 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 04:35:38 GMT
CMD []
```

-	Layers:
	-	`sha256:0b40b0bd0da3095d93bf74233a1d0bf638b2511fee461df8f6a71aad5a038589`  
		Last Modified: Wed, 29 Mar 2023 18:17:38 GMT  
		Size: 2.8 MB (2813760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5980c95097dfced199688de3f6aa45cd2216bfddef048561966b6608945af2f0`  
		Last Modified: Thu, 30 Mar 2023 04:38:24 GMT  
		Size: 46.3 MB (46321744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690ae6fe9c6e1be629171f54ae05b866b6572efa3b1d22692d741929e7d11bb7`  
		Last Modified: Thu, 30 Mar 2023 04:38:12 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:2fabb6c5fa95ead9711c9785ebab43a38eacb02b418775d6b5ab1a73fa8acc8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47598984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb61c9640b3da92089de86d78ac057c997e5d877f757120cda472c896b941e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:42:07 GMT
ADD file:5cf392863cd9a0735de88f9e7dab93c9e74aca59ca05b792943cf3b621ea2c59 in / 
# Wed, 29 Mar 2023 17:42:07 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 23:08:14 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_VERSION=7.3.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 29 Mar 2023 23:08:14 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Wed, 29 Mar 2023 23:08:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Wed, 29 Mar 2023 23:08:15 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 29 Mar 2023 23:08:15 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Wed, 29 Mar 2023 23:08:15 GMT
ENV VARNISH_SIZE=100M
# Wed, 29 Mar 2023 23:09:46 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Wed, 29 Mar 2023 23:09:47 GMT
WORKDIR /etc/varnish
# Wed, 29 Mar 2023 23:09:47 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 29 Mar 2023 23:09:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 29 Mar 2023 23:09:48 GMT
USER varnish
# Wed, 29 Mar 2023 23:09:48 GMT
EXPOSE 80 8443
# Wed, 29 Mar 2023 23:09:48 GMT
CMD []
```

-	Layers:
	-	`sha256:1536575ac9c5f5fff4522c60d4610af0a52be584c36e652080c6c0ad169d4f27`  
		Last Modified: Wed, 29 Mar 2023 17:42:42 GMT  
		Size: 2.6 MB (2610636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadb2417c7920374afa7798d98c70d2f0a8290f641bb3dbc112a2158ac097a2d`  
		Last Modified: Wed, 29 Mar 2023 23:12:02 GMT  
		Size: 45.0 MB (44987850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a556b2e0ae2040be8338c713604078ac74fa7ec335f48fff28337d8b007e52`  
		Last Modified: Wed, 29 Mar 2023 23:11:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:2f211fd175cf8d3b2803abe0bcc1b42a94c2557568e4f301340f18c517254acb
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
$ docker pull varnish@sha256:966e57e0f907166e5cfe74f03c70027a7bfeb7763d21ef6c0421f62415e9cde0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106798860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde7e0fae0241ca1def63efb79171503518a8488438150538534de27d6aa8e8e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:35:42 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 08:35:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 08:35:43 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 08:35:43 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 08:35:43 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 08:38:51 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 08:38:52 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 08:38:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 08:38:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 08:38:52 GMT
USER varnish
# Thu, 23 Mar 2023 08:38:52 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 08:38:52 GMT
CMD []
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ebc78fcc0bfd5f9a86a59c7ba9dc92d6c6ac286ed8792d8616139b3f728557`  
		Last Modified: Thu, 23 Mar 2023 08:44:29 GMT  
		Size: 75.4 MB (75386965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3679bcba66926e3e08e43f6a3b27ae9c5902dca3a35c8a3b5c4da60d413ff28d`  
		Last Modified: Thu, 23 Mar 2023 08:44:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:e853c6bce2a44d87519a8074817ef212fab243e6dd356a4abd7e512d7067617c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83146210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad755a8b29b5be4bc688f975df90490adc469fb52f225c1498c7796c7647faf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:27:26 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 12:27:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 12:27:26 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 12:27:26 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 12:27:27 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 12:30:37 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 12:30:37 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 12:30:38 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:30:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 12:30:38 GMT
USER varnish
# Thu, 23 Mar 2023 12:30:38 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 12:30:38 GMT
CMD []
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e2d8b662d5f484247a6608121d266efd1a66ababf38e85884f4b25c943a1b`  
		Last Modified: Thu, 23 Mar 2023 12:36:07 GMT  
		Size: 56.6 MB (56568388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e95c1272c5b14b209ef35f4b8e7b15c931bf708123d990755924aa025813cc`  
		Last Modified: Thu, 23 Mar 2023 12:36:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e5c5ffd6dc2c95d7fee3e5bcbf2d300bb9b0f33918460846e02bb0bc789617c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100588684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720135e26f679dcaa1eeddcd6ae73bb0c8c9cda47e9f248bc72656427f8d3bb5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:25:32 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 07:25:32 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 07:25:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 07:25:33 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:25:33 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:25:33 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:28:40 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:28:40 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:28:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:28:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:28:40 GMT
USER varnish
# Thu, 23 Mar 2023 07:28:40 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:28:41 GMT
CMD []
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88629f01162d8c785683ae0fbde30f240c471df8fb8aad45c270bea1517206`  
		Last Modified: Thu, 23 Mar 2023 07:33:28 GMT  
		Size: 70.5 MB (70525493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132c73bad44c61b38ee1ac99c3b7cbcedeb6aaf28804afc1b2f5e9cc4240a43`  
		Last Modified: Thu, 23 Mar 2023 07:33:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:d419b0f75d76108ac53df1fb2fe379af01c91466546b17a14308403e11c46a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108170833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb22f44ce303b7331ea25c68f9cc24123cc7caa128b2bd1d0017a321eefab0a9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:41:48 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 19:41:48 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 19:41:48 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 19:41:49 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 19:41:49 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 19:41:49 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 19:41:49 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 19:45:31 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 19:45:32 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 19:45:32 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:45:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 19:45:32 GMT
USER varnish
# Thu, 23 Mar 2023 19:45:32 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 19:45:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7201f33e2e4539694a92607b61b1e2ea1a53f436c5855d96029b9db6cd82dba`  
		Last Modified: Thu, 23 Mar 2023 19:52:07 GMT  
		Size: 75.8 MB (75774064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db12df95277ae5ee27785ea05ef6bebee5a443b7747e7e56cfef27b7f85b0230`  
		Last Modified: Thu, 23 Mar 2023 19:51:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:99a9dcf0cddca561abbcd5bc5b002adbb083de964d8746e3063cab564573c331
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106076410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e817121269101ae25eb3c824355809f156a4e72be8a908710817a5575d2fb848`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:43:55 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Wed, 12 Apr 2023 00:43:56 GMT
ARG VARNISH_VERSION=7.3.0
# Wed, 12 Apr 2023 00:43:56 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Wed, 12 Apr 2023 00:43:57 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Wed, 12 Apr 2023 00:43:57 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Wed, 12 Apr 2023 00:43:58 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 12 Apr 2023 00:43:58 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Wed, 12 Apr 2023 00:43:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Wed, 12 Apr 2023 00:43:59 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 12 Apr 2023 00:44:00 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Wed, 12 Apr 2023 00:44:00 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 Apr 2023 00:55:22 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 12 Apr 2023 00:55:26 GMT
WORKDIR /etc/varnish
# Wed, 12 Apr 2023 00:55:26 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 12 Apr 2023 00:55:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 Apr 2023 00:55:28 GMT
USER varnish
# Wed, 12 Apr 2023 00:55:28 GMT
EXPOSE 80 8443
# Wed, 12 Apr 2023 00:55:29 GMT
CMD []
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a23cf789a1d6f1a8f615b2f894ff5d23dfc1871bec09bf4ddc25dfc2f51729`  
		Last Modified: Wed, 12 Apr 2023 01:17:31 GMT  
		Size: 70.8 MB (70783923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f561be54d7ea2acd53189c9a5ceccfe7bcc785342020b6d142e731caa7146a85`  
		Last Modified: Wed, 12 Apr 2023 01:17:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:f748dab7db2aef4a89ab5fbba3270bb4b7b4a9d91769dd4a06b1dfeca1d57a22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87097616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dce21e8c45603a8701fccb74b85b9028709de3d15d63f820ea22a4dd38aea5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:04:15 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Thu, 23 Mar 2023 07:04:15 GMT
ARG VARNISH_VERSION=7.3.0
# Thu, 23 Mar 2023 07:04:15 GMT
ARG DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165
# Thu, 23 Mar 2023 07:04:15 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Thu, 23 Mar 2023 07:04:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Thu, 23 Mar 2023 07:04:16 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:04:16 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:04:16 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:06:51 GMT
# ARGS: DIST_SHA512=2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165 PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.0 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.0.tgz -o $tmpdir/orig.tgz;     echo "2693ed52dccc889e0bb1035ef1e3e5e12b8060ff3be6e6b78593b83f60408035649185dc29dd92265e18d362c3bff2f82cd74b7ae0aa68b94b40013824f3c165  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:06:53 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:06:53 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:06:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:06:53 GMT
USER varnish
# Thu, 23 Mar 2023 07:06:53 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:06:54 GMT
CMD []
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aed1e81cb3f95f54447b5519e283bea6931614c96f3725aa0df9795d68af88a`  
		Last Modified: Thu, 23 Mar 2023 07:11:51 GMT  
		Size: 57.5 MB (57450304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c04293d87cc93048f858704fab4e5c64021a66e803dbcb97a23b838db4cca7`  
		Last Modified: Thu, 23 Mar 2023 07:11:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old`

```console
$ docker pull varnish@sha256:8d70ffffd510634a21c7ecdf4a6b973b08232a9987bddd71a69d78770ab64952
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
$ docker pull varnish@sha256:51308e399b5bfb42c1acc656b5bb6593909e063e225d0194a72673bd68aba5b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106842482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8d5690ee4d009d1abc0f4765cc44d495ddcc5cf1c099161806ac0a9736aa75`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:39:07 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 08:39:07 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 08:39:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 08:39:07 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 08:39:07 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 08:39:07 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 08:41:46 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 08:41:46 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 08:41:46 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 08:41:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 08:41:46 GMT
USER varnish
# Thu, 23 Mar 2023 08:41:47 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 08:41:47 GMT
CMD []
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347377f781d4b09ab7508a61972fd4b3e5246b4e2bd9c35b6fd67626aa4fb2ab`  
		Last Modified: Thu, 23 Mar 2023 08:44:51 GMT  
		Size: 75.4 MB (75430587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3f25d148d89bd617db5fdf5fe5c6c6668b80541f6821f6d1b101c9b259b76`  
		Last Modified: Thu, 23 Mar 2023 08:44:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:39f08af282e300bee400d681a13589ce486241507ceb777d1769ef79323686aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83187971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82615d9cab07301c0432d7198b5a1b74147212fb524a83b9881f9ae48bb5ab13`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:30:49 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 12:30:49 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 12:30:49 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 12:30:49 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 12:30:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 12:30:50 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 12:30:50 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 12:30:50 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 12:33:25 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 12:33:25 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 12:33:25 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:33:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 12:33:25 GMT
USER varnish
# Thu, 23 Mar 2023 12:33:26 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 12:33:26 GMT
CMD []
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138fb1bcb671938644266a2d6e0a35f5d781da8f3acfa8ec3b07f941e3c20cfd`  
		Last Modified: Thu, 23 Mar 2023 12:36:26 GMT  
		Size: 56.6 MB (56610150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecaa76a7918e4f17046b400bf59db8beb63a63bc17cb6ce56b7a9548f7bf8af`  
		Last Modified: Thu, 23 Mar 2023 12:36:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:266e9b50c88374c3169d686d798296050143e8fdb078a9cd5953a573a7d62f6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100868360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e23fa80f9496e9f34877c07b18fe4710a89f6d7f7c5daccfa8891adcb970433`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:28:56 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 07:28:56 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 07:28:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 07:28:56 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:28:57 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:28:57 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:31:16 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:31:16 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:31:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:31:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:31:17 GMT
USER varnish
# Thu, 23 Mar 2023 07:31:17 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:31:17 GMT
CMD []
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25386ca99e6fa25d37d6be5b3c0712ff9cccffb73dc9ce32937bb13dc65999b7`  
		Last Modified: Thu, 23 Mar 2023 07:33:46 GMT  
		Size: 70.8 MB (70805167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88ce616ecea4f7377751a315243e6fd13702ec941bfeb1254732c6c14cb7f38`  
		Last Modified: Thu, 23 Mar 2023 07:33:39 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:c5847816dbbba69f71abce18fe4e24d6884a124c2f34ed0ad714b0547784056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108227006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfc7fdeefdec180ace517aae569c98d739b6bbbc071ac199b6c96b3a43e1e6b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:45:42 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 19:45:42 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 19:45:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 19:45:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 19:45:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 19:45:43 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 19:45:43 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 19:45:43 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 19:49:01 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 19:49:02 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 19:49:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:49:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 19:49:02 GMT
USER varnish
# Thu, 23 Mar 2023 19:49:02 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 19:49:02 GMT
CMD []
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a361541ee32822f6a5bcc2a2f6f08634cfe9d2cbc9b31e6ff456e3ac1488bc`  
		Last Modified: Thu, 23 Mar 2023 19:52:34 GMT  
		Size: 75.8 MB (75830240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37baffbfd4dfac65be48e4991e66887a684b81abc578406df0cea4592e054b91`  
		Last Modified: Thu, 23 Mar 2023 19:52:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:2ddbd11558d86d08b3f82a25da574d70734fed468550edb4d6b957cf2fc4ff55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106112382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fcc671da9acaf8ae312a5ba85fd3d77e7e1b88a900054ac23433f6dad4b7cde`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:55:40 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Wed, 12 Apr 2023 00:55:40 GMT
ARG VARNISH_VERSION=7.2.1
# Wed, 12 Apr 2023 00:55:41 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Wed, 12 Apr 2023 00:55:41 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Wed, 12 Apr 2023 00:55:42 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Wed, 12 Apr 2023 00:55:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 12 Apr 2023 00:55:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Wed, 12 Apr 2023 00:55:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Wed, 12 Apr 2023 00:55:44 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 12 Apr 2023 00:55:45 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Wed, 12 Apr 2023 00:55:45 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 Apr 2023 01:06:37 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 12 Apr 2023 01:06:41 GMT
WORKDIR /etc/varnish
# Wed, 12 Apr 2023 01:06:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:06:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 Apr 2023 01:06:43 GMT
USER varnish
# Wed, 12 Apr 2023 01:06:43 GMT
EXPOSE 80 8443
# Wed, 12 Apr 2023 01:06:45 GMT
CMD []
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4a89d7f741d3117b0ee6c2f7194da63a2eb7e31a212514121c21a0f9a2d56d`  
		Last Modified: Wed, 12 Apr 2023 01:18:03 GMT  
		Size: 70.8 MB (70819898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3fec9bc4ead77e694d7ee941f4809ba1dc75a4379c2e14982a287a907f61d2`  
		Last Modified: Wed, 12 Apr 2023 01:17:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:a828400ea054dd296391072926707f18eb07be46812e335f5171c1cb838621b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87138814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382ad2c68c00cbb928f0c3c2bdc525e23bbeb36107ce85428f3155f0525265da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:07:08 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 23 Mar 2023 07:07:09 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 23 Mar 2023 07:07:09 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 23 Mar 2023 07:07:09 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 23 Mar 2023 07:07:09 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Thu, 23 Mar 2023 07:07:09 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:09:29 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Thu, 23 Mar 2023 07:09:32 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:09:32 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:09:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:09:32 GMT
USER varnish
# Thu, 23 Mar 2023 07:09:32 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c80f77587a5dfe7c42be2aa5ec37fb62f7b9e9b8d92f302c306132a915684e`  
		Last Modified: Thu, 23 Mar 2023 07:12:05 GMT  
		Size: 57.5 MB (57491504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2feadb32de32ec44136c747758376b15f1fcd05d3cabc73325bbf1eb070b33`  
		Last Modified: Thu, 23 Mar 2023 07:11:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:4afc17b0aa7c483b822ae0c548f93d87fdcfc38715e30734657bad8a3171f534
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
$ docker pull varnish@sha256:a320ad063c3556dfea1308e7747a7b74de2e6580bb136653f10480b192d2b7ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59399546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619a779899e4b887658162b42b9f51b181570836a20e93eabacd1c0634421c23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:16:18 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 02:16:18 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 02:16:18 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 02:16:19 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 02:16:19 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 02:16:19 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 02:16:19 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 02:17:35 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 02:17:35 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 02:17:35 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 02:17:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 02:17:35 GMT
USER varnish
# Thu, 30 Mar 2023 02:17:35 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 02:17:36 GMT
CMD []
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c114fe4204a2c955105dd5cd8a42a772594a1642947fbefba511406b0e60e5`  
		Last Modified: Thu, 30 Mar 2023 02:18:20 GMT  
		Size: 56.6 MB (56572454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debea196e0761731bed241b5b0124d7dab6070192ebf9f49532117ef228a4fd7`  
		Last Modified: Thu, 30 Mar 2023 02:18:13 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:fccf7f20e1622e5cc7de9c8a0374d530f4ce08e15bae3fa806e6c5f34100a250
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ac3c9362d31494b1482831d5f9600db9a9423084b5bcdfb6bf502d29be4134`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:05:06 GMT
ADD file:0516b2e2d8a5c0a3e85e67a20375312bdc586a63094d779b9ac92517cf74a19d in / 
# Wed, 29 Mar 2023 18:05:06 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:16:02 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 00:16:02 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 00:16:02 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 00:16:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 00:16:03 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 00:16:03 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 00:16:03 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 00:17:15 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 00:17:16 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 00:17:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 00:17:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 00:17:16 GMT
USER varnish
# Thu, 30 Mar 2023 00:17:16 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 00:17:16 GMT
CMD []
```

-	Layers:
	-	`sha256:fafb00bc68cf26e4a27ad2dce7303945ba9e40994e77c9269e610e0452ae9dce`  
		Last Modified: Wed, 29 Mar 2023 18:07:17 GMT  
		Size: 2.4 MB (2437606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7ec1086689ab0fd73293e70d501d454a27eb5ea261d03a2430cb0d14696427`  
		Last Modified: Sat, 08 Apr 2023 02:41:03 GMT  
		Size: 42.7 MB (42710102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9ac18a355d90f33336fbada96e19569338d541feae42ae2d313ce006609bb1`  
		Last Modified: Sat, 08 Apr 2023 02:40:57 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:4b01c566b91d765af9c55ca58772d6926b481ba4c60bfe7b9d6b0adca255f10b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52139702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3552cf8b859208887e19e7d4ff64ae304e14cf411f5dadeb80d6c52b607f72d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:39:22 GMT
ADD file:4acfda16c71abce07068ed23839e9de60c1d1145ab8002b3a92c15b1e80d4356 in / 
# Wed, 29 Mar 2023 17:39:23 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:55:19 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 05:55:20 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 05:55:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 05:55:20 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 05:55:20 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 05:55:20 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 05:56:25 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 05:56:25 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 05:56:25 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 05:56:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 05:56:26 GMT
USER varnish
# Thu, 30 Mar 2023 05:56:26 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 05:56:26 GMT
CMD []
```

-	Layers:
	-	`sha256:60a00c11adf5202a365ec8215b889c3390d67fa295ab79940e1c5dc4cbed9db1`  
		Last Modified: Wed, 29 Mar 2023 17:40:04 GMT  
		Size: 2.7 MB (2722002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c53d05c94805192159ec306400f8402f101647b10b4f2862a4b9cafe6d9ea95`  
		Last Modified: Thu, 30 Mar 2023 05:57:04 GMT  
		Size: 49.4 MB (49417204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfbbc1899969f2944b32d817962c27670200b641a7ff5b382026a2a6f1e91f8`  
		Last Modified: Thu, 30 Mar 2023 05:56:58 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b4aed57dfb69759cbbf97f8251f733ed209e5377c0b138e878768446cf3f1012
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59579474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2d5054f0237342f09e7c81d57f5b91b2a7258c98c54862bcd60b70f213eff4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:36:10 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 01:36:10 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 01:36:10 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 01:36:11 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 01:36:11 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 01:36:11 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 01:38:03 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 01:38:03 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 01:38:03 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 01:38:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 01:38:03 GMT
USER varnish
# Thu, 30 Mar 2023 01:38:04 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 01:38:04 GMT
CMD []
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec17ca4c36e5d196286fcd4f66f0a6879ff35841617edc48c24a2b0d3fed6c5`  
		Last Modified: Thu, 30 Mar 2023 01:39:02 GMT  
		Size: 56.7 MB (56746401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acb1c0b2cc2ca1f40568c89f6ace8d204192474b0b299f6afbd1d5b87c89ad4`  
		Last Modified: Thu, 30 Mar 2023 01:38:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:47175a4b9a3d7cc10400bda61c20d308651152bf93f3268aa3b4c850c4cebb3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49172829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe520b41ef8593a0ca87c4b15e445248e7728729026968d7c7167a33b40a8e28`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 18:16:40 GMT
ADD file:3c2a8d553fa0998f13f86592f104a9a4ad14f8db46dfa9145c8fbbca0b87ee9a in / 
# Wed, 29 Mar 2023 18:16:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:35:48 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Thu, 30 Mar 2023 04:35:48 GMT
ARG VARNISH_VERSION=7.2.1
# Thu, 30 Mar 2023 04:35:49 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Thu, 30 Mar 2023 04:35:49 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Thu, 30 Mar 2023 04:35:49 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Thu, 30 Mar 2023 04:35:50 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Thu, 30 Mar 2023 04:35:50 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Thu, 30 Mar 2023 04:35:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Thu, 30 Mar 2023 04:35:51 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Thu, 30 Mar 2023 04:35:51 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Thu, 30 Mar 2023 04:35:51 GMT
ENV VARNISH_SIZE=100M
# Thu, 30 Mar 2023 04:37:42 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Thu, 30 Mar 2023 04:37:43 GMT
WORKDIR /etc/varnish
# Thu, 30 Mar 2023 04:37:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 30 Mar 2023 04:37:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 30 Mar 2023 04:37:44 GMT
USER varnish
# Thu, 30 Mar 2023 04:37:45 GMT
EXPOSE 80 8443
# Thu, 30 Mar 2023 04:37:45 GMT
CMD []
```

-	Layers:
	-	`sha256:0b40b0bd0da3095d93bf74233a1d0bf638b2511fee461df8f6a71aad5a038589`  
		Last Modified: Wed, 29 Mar 2023 18:17:38 GMT  
		Size: 2.8 MB (2813760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69361e01f667423c0f2d961984f6e7db1a81226574e2f2e13b25de56a1ed714d`  
		Last Modified: Thu, 30 Mar 2023 04:38:48 GMT  
		Size: 46.4 MB (46358574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b033b092d98a898fd606406859a2bdc093c0babde613a26ed82fff5736c9290`  
		Last Modified: Thu, 30 Mar 2023 04:38:37 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:cae32a9f29cd9997a1fe2ee6f8d0b8e3ff91c21e6213716d9ac34675317dc70d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47646967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e24f77bba538e7715318a014e47a2ab4183cd521c07f85ecc3a82ab13ed2830`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 29 Mar 2023 17:42:07 GMT
ADD file:5cf392863cd9a0735de88f9e7dab93c9e74aca59ca05b792943cf3b621ea2c59 in / 
# Wed, 29 Mar 2023 17:42:07 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 23:10:06 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VARNISH_VERSION=7.2.1
# Wed, 29 Mar 2023 23:10:06 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47
# Wed, 29 Mar 2023 23:10:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a
# Wed, 29 Mar 2023 23:10:07 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 29 Mar 2023 23:10:07 GMT
ENV VMOD_DEPS=automake curl libtool make pkgconfig py3-sphinx
# Wed, 29 Mar 2023 23:10:07 GMT
ENV VARNISH_SIZE=100M
# Wed, 29 Mar 2023 23:11:26 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=5c702fa6c3a88882a2678f75161692762e7d6c47 VMOD_DYNAMIC_SHA512SUM=3503ae09bae731213d5a6823af9fb758bcbcaf06678a2a0efc0b35d9f1b18ab46e02f02b75db8a4858bb2b623e76ea253e65ef2ae3ab076558b52b414996d33a VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;     adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Wed, 29 Mar 2023 23:11:28 GMT
WORKDIR /etc/varnish
# Wed, 29 Mar 2023 23:11:28 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 29 Mar 2023 23:11:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 29 Mar 2023 23:11:28 GMT
USER varnish
# Wed, 29 Mar 2023 23:11:28 GMT
EXPOSE 80 8443
# Wed, 29 Mar 2023 23:11:28 GMT
CMD []
```

-	Layers:
	-	`sha256:1536575ac9c5f5fff4522c60d4610af0a52be584c36e652080c6c0ad169d4f27`  
		Last Modified: Wed, 29 Mar 2023 17:42:42 GMT  
		Size: 2.6 MB (2610636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091447cbd58b57bbe1eb2edf62b5e2d9c06467104aebfc70c02d7cfafa01868c`  
		Last Modified: Wed, 29 Mar 2023 23:12:17 GMT  
		Size: 45.0 MB (45035834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390574d541f53e2036c226ec79255c18a2429053de04847092de875c4925890b`  
		Last Modified: Wed, 29 Mar 2023 23:12:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:fcf64330415f4e2dbae5116152341b21ca016778361f27e2e78cb8633fd58fb6
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
$ docker pull varnish@sha256:454bde26abe856c11f2c01e49ee4972295c529ca8d572cfd5ac7458c09dc7c6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100653611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bff958899eb177d68ddf3857432ca3caa2c29e9ac61fd74266988574660a054`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:42:01 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 08:44:02 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 08:44:03 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 08:44:03 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 08:44:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 08:44:03 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 08:44:03 GMT
CMD []
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ac5fdbdd5295f4e6ef96170d4b6072fdf64ef67b1fce4835037b8e91c3efc`  
		Last Modified: Thu, 23 Mar 2023 08:45:10 GMT  
		Size: 69.2 MB (69241506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d0a5f8d42b9a02bd2d685179c8010def08c6e8fb512917c1b65d918a108708`  
		Last Modified: Thu, 23 Mar 2023 08:45:01 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:aa0c080cc1b68eb694be57b394774e620d299b46e207685c03e249eb5e8f825f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77228234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7bcdaeade43ceb79e0ad2ce826942782ec2c48f3ab24bf6391af43b6ec472d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:33:43 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 12:35:40 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 12:35:40 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 12:35:41 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:35:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 12:35:41 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 12:35:41 GMT
CMD []
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5c7c592dd5fd3a325f43dc46c9e39c39c7d4794449157ba636890dc521693e`  
		Last Modified: Thu, 23 Mar 2023 12:36:44 GMT  
		Size: 50.7 MB (50650203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4cd2918617aa3fb3c34f6df728ce7c6d3c5008bcfe5ffad004354ccfba130d`  
		Last Modified: Thu, 23 Mar 2023 12:36:37 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:57ffc6a9acfa003a371ad0f81185cd8e35a1d03c963e6aef8bf3533763232a5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94715614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825eaf119d4795f7c54fd830d8e1b86f368d0809890c546995db8817ef82903f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:31:19 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:33:04 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 07:33:05 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:33:05 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:33:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:33:05 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:33:05 GMT
CMD []
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbe80000c70973cea6a6fa729ec97b0ede579e55bbaa11d96bc10fa1c819c2e`  
		Last Modified: Thu, 23 Mar 2023 07:34:03 GMT  
		Size: 64.7 MB (64652214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe7aba80bb8f6017efb994e2fe82ac30bf71b1729158636187278db132a9604`  
		Last Modified: Thu, 23 Mar 2023 07:33:56 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:c634b629b6af576f45d9b34884348979e02256af100ffd6601292658628883bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102080872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e480b2929c4a10c95ad4650a1b25a698b5deb5141a84e55d5f41c96b723a87d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 19:49:06 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 19:51:28 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 19:51:29 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 19:51:29 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:51:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 19:51:29 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 19:51:29 GMT
CMD []
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27296d9a8485bf51ab09c6030604be9818738e92acf93431ab9c2e11f2b6cddb`  
		Last Modified: Thu, 23 Mar 2023 19:52:56 GMT  
		Size: 69.7 MB (69683895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221df35ede9e1583031e7125c18605249d41d70d719ca12c66a36ea7f33232bd`  
		Last Modified: Thu, 23 Mar 2023 19:52:44 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:18bd3322c2f9ccc96bfce197018af7ff9306a5913379476af9c84e061e770095
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99803629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f0683fd328a003ec4c95f0c7d93bb88582d34cba7b9ea9a048b186914841c5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 Apr 2023 01:16:48 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 12 Apr 2023 01:16:52 GMT
WORKDIR /etc/varnish
# Wed, 12 Apr 2023 01:16:52 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 Apr 2023 01:16:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 Apr 2023 01:16:53 GMT
EXPOSE 80 8443
# Wed, 12 Apr 2023 01:16:54 GMT
CMD []
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c91ede6f2abd53adaec518fad85de307f689c38e8eab390a7359e142ae3a16`  
		Last Modified: Wed, 12 Apr 2023 01:18:31 GMT  
		Size: 64.5 MB (64510930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd33a842deca9de4a3e249248620b5666ab2fa35cae6fe8b10b79955f955c3e`  
		Last Modified: Wed, 12 Apr 2023 01:18:15 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:69bd5fff0a8ca56a5c8272ac0f401cb954f762a2b6ad65a51a0cbccfff195261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81000136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d407fac676df9e15e1ff341197bbb641128b56d81f1cdf706502a3899e984ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:09:46 GMT
ENV VARNISH_SIZE=100M
# Thu, 23 Mar 2023 07:11:24 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 23 Mar 2023 07:11:26 GMT
WORKDIR /etc/varnish
# Thu, 23 Mar 2023 07:11:26 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:11:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 23 Mar 2023 07:11:26 GMT
EXPOSE 80 8443
# Thu, 23 Mar 2023 07:11:26 GMT
CMD []
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e74619a3634d4edc8b607a852318272e94e45a43dd1bc3100b88df9c04cba60`  
		Last Modified: Thu, 23 Mar 2023 07:12:18 GMT  
		Size: 51.4 MB (51352615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b41672e050ea9a532388b3c2f5061371da1182a77e33f532128654fbd98fdc`  
		Last Modified: Thu, 23 Mar 2023 07:12:12 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
