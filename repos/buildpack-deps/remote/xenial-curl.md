## `buildpack-deps:xenial-curl`

```console
$ docker pull buildpack-deps@sha256:01b9bdb668589ea8e2049c41769ea9621a1976f894bdabbad0bb108d265cb146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:xenial-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0144acaf40f989d22658269b9374fbf4d4f42e995e12318aa35ef6367ff6f141
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51607419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdda0b544105c882fb40d319c150aa107347803df512ced409c8c03adcd705ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:09:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:09:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28f4fbc8f95e6f96e8ebaf99fc8370a6bf2d69a5aaad0605ca75d6b2055c987`  
		Last Modified: Wed, 17 Jun 2020 02:16:22 GMT  
		Size: 7.3 MB (7285591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:30d2a7505d601b6cf1cee76aed105c0cb1bc88aaf985909a3decdf7584956b7e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45100473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc215be3e9b38a9221e10db6ea9c6a1ffc575e905d3d293fe4bf243ec46a591d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 02:04:31 GMT
ADD file:6cc12f5b0908f30b9097dd8947a769888e2fed5c2a25671d1e4cd93ac0ef7a2a in / 
# Wed, 17 Jun 2020 02:04:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:04:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 02:05:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 02:05:12 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:43:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:964b1ad4ea33c6edf524b0fba723b83aa90e37a66419cf5e514392304bd73309`  
		Last Modified: Mon, 18 May 2020 15:50:57 GMT  
		Size: 39.0 MB (38964390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b1c0566b01f5b9247bdf23fee3adfd14071d248058523063939ce8c482863c`  
		Last Modified: Wed, 17 Jun 2020 02:05:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5534a4581c7bc4061f7f3c35130d6daa15345f5791fe5c4c90cbe06def252991`  
		Last Modified: Wed, 17 Jun 2020 02:05:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0db3772af551e10afa4bced33b87cf3a0716943e901e4a9da41b1caac84b55`  
		Last Modified: Wed, 17 Jun 2020 02:05:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b278ad964fd160d99e9ddc624867de7dd1928e6d1b2d57e8761791c5d511d77`  
		Last Modified: Wed, 17 Jun 2020 02:50:28 GMT  
		Size: 6.1 MB (6134556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3cfbcc8c45de8ed7c45fd2ed022c702d377d4e5609e9591393fbb38132c4dcd7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46347649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60682a3f53061b6dff0ab6f3e8766791ad69c438ad9e454c67fda04a358843f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:29:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:29:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719c4f98cdfa1b94b180a6679d163ca4158b94cd0c07c451bd37677caba1afdf`  
		Last Modified: Wed, 17 Jun 2020 02:39:05 GMT  
		Size: 6.3 MB (6342219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ed4546f958f2ae03e5d9828016ed4f83922dc7f5753afa2818c8b0ed280b3733
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe3ef3e5b07bc69d45809f2ec0d689a8e779ff283e12f90274a3cd1ce310e20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:39:24 GMT
ADD file:59bc1e3c513e2a53f34d3c366fbd90221f9f66cc28580092ad98761704e297c2 in / 
# Wed, 17 Jun 2020 01:39:25 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:39:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:39:27 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:39:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:04:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:886386dac43ac74334fbfea18a9bdd374fea3c200e555719e76e3c8ab4a42b24`  
		Last Modified: Mon, 18 May 2020 15:50:47 GMT  
		Size: 44.3 MB (44256143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8e8acdf7169f36f991a88019ded1aa3b079e34a068e816f23b5cc36b39e45c`  
		Last Modified: Wed, 17 Jun 2020 01:40:03 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4082258b52ba5c66a1b6ffcc2d870f1bc91bf8d76a23f3bf77cf6fe1d77b91c6`  
		Last Modified: Wed, 17 Jun 2020 01:40:02 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede304431cec0498213d3a4a9c15ef75cf249e7c83825ba0c7ad3274308934ad`  
		Last Modified: Wed, 17 Jun 2020 01:40:03 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d91010a19dec56e92a1a1ffd0979a27787ae3c295a5ffdfdabb3fa082afdfa`  
		Last Modified: Wed, 17 Jun 2020 02:10:00 GMT  
		Size: 7.4 MB (7428894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:df5cd585fa5031e59bf6a55e29c1d8976f9ad1484d01e7369687a755a171db57
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53362781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15e2c469b4c6a9d5d4249e2d9811eb221f09c6370fff92046f497ff706959b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:27:13 GMT
ADD file:d522ca8cc867b1005aecf011d2ebce51b45c03f4a939ff6402b93677899b6deb in / 
# Wed, 17 Jun 2020 01:27:26 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:27:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:27:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:27:46 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:02:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:02:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4e5edfd8804acbddee0cc3d44c618a9b6091d13eed1ee94389f0582dd6e1517f`  
		Last Modified: Mon, 18 May 2020 15:51:40 GMT  
		Size: 46.2 MB (46175202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f957dd8506a4f76ec7e46e59773faf6c8b06035c6efb16135ac9dd052c7c28ef`  
		Last Modified: Wed, 17 Jun 2020 01:29:40 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f405a18af8f06aed09d754b2dfa5895076d09ec15a74e48406cb51a11779e0`  
		Last Modified: Wed, 17 Jun 2020 01:29:39 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8467f4c0538fe8863f2b0ee45e8b91f6a89337b16dc34624ef60cce0c18675`  
		Last Modified: Wed, 17 Jun 2020 01:29:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecc9fab4fcbe297dfe3ff8a3f7fdacdf73972ee410e8ae9d95afb7022c517c8`  
		Last Modified: Wed, 17 Jun 2020 03:23:51 GMT  
		Size: 7.2 MB (7186073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:07c52073b2d79fd067aab84d5eb5463c6a38de81e898256abd8a87c1b3c3a13d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49901703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2846ebec249c4e53a646c1a8e9f030e48c0f6e5d0c49b96563b77de326bb6d35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:35 GMT
ADD file:10bdfc967b8d5968cd7b7364aa8e93b3c2516128d782e6ef85dbc4a7f83e4b7a in / 
# Wed, 17 Jun 2020 01:42:38 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:42:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:40 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:43:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:43:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d0a0ed0c47429688bb895e35ebcd84f8b5bbd593eac2f0151603dd77dc50069e`  
		Last Modified: Mon, 18 May 2020 15:51:52 GMT  
		Size: 42.9 MB (42880585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81edf201d946558ead9d7e8425aec01524979f0532cb691919fe10d4dc3de238`  
		Last Modified: Wed, 17 Jun 2020 01:43:37 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141251eec5140d685bca36b9c230fd293ae4af1e90c04b66e7b2cf84bcea2010`  
		Last Modified: Wed, 17 Jun 2020 01:43:37 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4537a6d0859ba64cb05517eb056a0afb61ce29c65c43f9f8ddb388b4f6f75e90`  
		Last Modified: Wed, 17 Jun 2020 01:43:37 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6146265980b57663866b6f735db1d50b5990895e4a9ac4aaaeaf2d1c073a65b`  
		Last Modified: Wed, 17 Jun 2020 02:56:49 GMT  
		Size: 7.0 MB (7019632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
