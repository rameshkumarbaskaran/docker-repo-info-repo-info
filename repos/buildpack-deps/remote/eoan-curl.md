## `buildpack-deps:eoan-curl`

```console
$ docker pull buildpack-deps@sha256:7671ad1792f12e361c7ac6d102f42e7ef0f104e7b10da51dff488150bb054011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:eoan-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2d658f4deaa0e0247ba1be0483ea51fb9435bb769d7ecb143bb17cf46c338445
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38323934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a7d17835490fada55039e59139e729496e311d933602da0da07a5f9b025333`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:42 GMT
ADD file:f7e262b5b83427ba392961a76f015b60b140c12e8313ec3a5764b9829926a687 in / 
# Wed, 17 Jun 2020 01:20:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:44 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 01:59:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:59:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3f2411103a12c8e169df7a9ea00ff26ab07501858e3eff315a2e11c219e78ce1`  
		Last Modified: Tue, 09 Jun 2020 20:51:11 GMT  
		Size: 28.3 MB (28261433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da04088b2c299c17ae8a78858846c6fd4a6c36717baa816974cc75bef632871`  
		Last Modified: Wed, 17 Jun 2020 01:21:53 GMT  
		Size: 30.6 KB (30640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1184837b6f6f4a130c8b4eb72f576b86c4c46b3e33dada4740a966948d98e6`  
		Last Modified: Wed, 17 Jun 2020 01:21:53 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354c6da61dcc176c5b363ded571bea1de41b718131658fa0e563f2a749028cd1`  
		Last Modified: Wed, 17 Jun 2020 01:21:53 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a9187cd317f7b194fecbc5f1650c2c058a745867f75de00303ca6164f84d9d`  
		Last Modified: Wed, 17 Jun 2020 02:13:26 GMT  
		Size: 6.5 MB (6513812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4357e28c21183158d80ed73cb61a69c0a4de0643f020f19c7985fd99939f89`  
		Last Modified: Wed, 17 Jun 2020 02:13:25 GMT  
		Size: 3.5 MB (3517039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3ac673c73b1cb31444249b54d62debd08373bed3c8c0b212512fdc439ea413c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32283574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f9080959c5c746d66b859c4f9bd5ef7dfa4c4844cea783c9ae6378a92a2ca4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 23 Apr 2020 22:06:26 GMT
ADD file:a786d9ae5b3aaa37e3188ec13cba2efb20951cc432a05a3695210ce018439ce0 in / 
# Thu, 23 Apr 2020 22:06:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 22:06:43 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 22:06:45 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 22:06:46 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 12:25:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 12:26:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8729ee1b2c9c364007cc8f9967331e0464ea4d2ce5998811ea52e890737a4b7c`  
		Last Modified: Mon, 13 Apr 2020 15:44:38 GMT  
		Size: 23.7 MB (23735820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7153a6c4736e5469da08e1b45afdaeb7aa5d7864a7396c35f7799afb2a8c96c6`  
		Last Modified: Thu, 23 Apr 2020 22:08:32 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2419c576e579e9eefaa1f9e5f5d8db949d4c09a789a577994d0f7237c35d4f9`  
		Last Modified: Thu, 23 Apr 2020 22:08:32 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f176618d72c6c467923dece921be857a756d30afd87f213c8658361102d14f3`  
		Last Modified: Thu, 23 Apr 2020 22:08:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b30b5dbb14c906a07aad7e49910a2a3bc2e2ce5a1e57c0c37c05fc801283301`  
		Last Modified: Fri, 24 Apr 2020 12:48:16 GMT  
		Size: 5.5 MB (5532892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48e073ec876479cc7eb8ae1cbe14afe25278c91ed319f83848df30560962f12`  
		Last Modified: Fri, 24 Apr 2020 12:48:15 GMT  
		Size: 3.0 MB (2983204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c9de5d0bc1be8c9356372b0b05200b5b66e9033da21bafac95118f59c72c570f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36770768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd7de0468b11ceb4702f1f679675e766c61bfaff6ba369ac3116f0db5c2c99b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:02 GMT
ADD file:afbae8593c2a310485f9ac20a2133d643aa78f1f287db87e1087832b0ea18b1e in / 
# Wed, 17 Jun 2020 01:43:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:10 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:16:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:16:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d1afa64cae883b0ec934e8fbc2f830e304f115308af38eaf523297c4f609d268`  
		Last Modified: Tue, 09 Jun 2020 20:52:04 GMT  
		Size: 26.9 MB (26856827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf5c9b0975d3d817466789f94fcfcc93d62ab7b6d979a9aa142836b712b047`  
		Last Modified: Wed, 17 Jun 2020 01:45:00 GMT  
		Size: 30.5 KB (30454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522f9d93dd776c07db2beae6d659ea57f4129e53d53995f5b39925911ac873c8`  
		Last Modified: Wed, 17 Jun 2020 01:45:00 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87211bb3d9b9ceb47475623e94327d188e9a61a929af9908773d610bc4da51a0`  
		Last Modified: Wed, 17 Jun 2020 01:45:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fd4bdf0856ce4ef79c137ebd9daa48e62b5ade607c3227cf1ba5bf264a8d17`  
		Last Modified: Wed, 17 Jun 2020 02:35:01 GMT  
		Size: 6.4 MB (6370589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c2dc4fa12cb39c777fb38247574583a980ae89bf17ccc90d27f0ab3d3aa69d`  
		Last Modified: Wed, 17 Jun 2020 02:35:00 GMT  
		Size: 3.5 MB (3511857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ba56ede574c1c70964e20822259ab88ae61f22d036113b2c0bd9ccc1136defe8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39720735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea1b7fff34b18e63fd97724cdb694de0c42856cbd2b29ec137c50e2e78ac20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:39:02 GMT
ADD file:40320578d00c1821c8821f38e2a57315d599aed7b8fc7d9802b43c61a68f542c in / 
# Wed, 17 Jun 2020 01:39:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:39:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:39:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:39:04 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:00:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:00:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8c36fa2111ce9dcde83dd801ec64601f6c2b3c088bdcc38e9b6e1ccb6309b7f1`  
		Last Modified: Tue, 09 Jun 2020 20:51:41 GMT  
		Size: 29.0 MB (29035230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fa8cf01bad05acfd29371595c17cde6b9391303a29ac2ec1f6eb6841aef676`  
		Last Modified: Wed, 17 Jun 2020 01:39:49 GMT  
		Size: 30.7 KB (30719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19249f6bd8f71396680b10c2143643495fca3f6366bf9aec8520fd0190be7072`  
		Last Modified: Wed, 17 Jun 2020 01:39:49 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0944949ff614b039740df9433ab1d4992a6c0bf629dbcffe5795305c3b8898`  
		Last Modified: Wed, 17 Jun 2020 01:39:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bbc19c077e82d808d2be92c96e0b006d38de91a3f98a2d7f6397d5c537e59c`  
		Last Modified: Wed, 17 Jun 2020 02:08:53 GMT  
		Size: 6.8 MB (6843100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09935cd525a610ed6f45f15d31f8b6d63ab85b522334543d9fbc4865137b37d1`  
		Last Modified: Wed, 17 Jun 2020 02:08:52 GMT  
		Size: 3.8 MB (3810677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9f2df4d1a713ef2f4daec6019134dc0973fc007507dbc436625330f99d5195d8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44902400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e5b7e30cc7ed028ee2e7248ac74cbc2f52c1bbd9d14a966921af1eeec8933b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 23 Apr 2020 20:43:51 GMT
ADD file:3dddd0440bd0461ad738de1cac6d91b3e135f8ced829fe6b4ce68191764cbead in / 
# Thu, 23 Apr 2020 20:43:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:44:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:44:13 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:44:15 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 12:36:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 12:37:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:92f1850658c279ede8a91155ce8c3448f24f41b6c34af2f7abc1758aa4b66da4`  
		Last Modified: Mon, 13 Apr 2020 15:45:23 GMT  
		Size: 33.0 MB (32986779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f77e23c3391871551319f5a95d13da7decaa4c5f82a6d8c5b7973466c8c759c`  
		Last Modified: Thu, 23 Apr 2020 20:49:15 GMT  
		Size: 30.5 KB (30496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d25529fd9371ec1a0256e037a3910b37015b517f876f30df0199a34a41c829`  
		Last Modified: Thu, 23 Apr 2020 20:49:15 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b901c3c78abc835c6887d98a6580e4b895cf612c470f317f39e5f46e2dbca0`  
		Last Modified: Thu, 23 Apr 2020 20:49:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02305273ba52f9a855a78ea8cb39ff2c511ec15e644f25c39aa6d0c371a6400`  
		Last Modified: Fri, 24 Apr 2020 13:18:57 GMT  
		Size: 7.4 MB (7420786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00441024500c01b26667ba67bf1ebccafcc416ef344b804c94baa59065a2c354`  
		Last Modified: Fri, 24 Apr 2020 13:18:56 GMT  
		Size: 4.5 MB (4463295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:54f282009099c9a4c7fde2d93a8a066f05a4ec03951f6b5cff27c76f70aadaab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36288087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340bb60537454a1cb269b2cdf5c61e1601ea595324495dd3a65d52a68f3579cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:44 GMT
ADD file:590238292f6a053ea2bf6e08f583c7d381c15ead1a8a0f1bad600fca48d20648 in / 
# Thu, 23 Apr 2020 17:52:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:56 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:49:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:49:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4a7e39a0b3f9ba3421a213b5b6ae19b4ee4315b5aff0252496ef8117c7caae2e`  
		Last Modified: Mon, 13 Apr 2020 15:45:44 GMT  
		Size: 26.7 MB (26682562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15519bbe785a81349f4b9318ec98f07fb1d7ed9742eaf004a27806254935f5bf`  
		Last Modified: Thu, 23 Apr 2020 17:54:25 GMT  
		Size: 31.1 KB (31106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39a183d313a7aec756ef4cec9ebed83e7eefb892c64f68a74fb640abde8a647`  
		Last Modified: Thu, 23 Apr 2020 17:54:25 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0914614caf2827873d1d4b1f12426334285b8d984af44e48b64b7db18c3ee4fc`  
		Last Modified: Thu, 23 Apr 2020 17:54:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba99f74f403727ed8ce2e6a910248a0a53edf2bff04fe4fe7551ee0acbaaf849`  
		Last Modified: Fri, 24 Apr 2020 07:55:26 GMT  
		Size: 6.1 MB (6139662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7833d62efa3405cf0f7f73e663802e5167b8fe4fc84628bdc4e14a161891379`  
		Last Modified: Fri, 24 Apr 2020 07:55:26 GMT  
		Size: 3.4 MB (3433720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
