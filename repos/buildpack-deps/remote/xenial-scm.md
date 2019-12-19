## `buildpack-deps:xenial-scm`

```console
$ docker pull buildpack-deps@sha256:11064878139c5b4dd064d301852be5d30c05809eb601102d765087a558ba23be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:xenial-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9a72467bff6b002a928058f69456bac6c65ab88d5a39eade145468ab8013f33a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c988311f71d5beccbfc3ce01b14b41602c4509832fd1c3581eef4e584b477698`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:36:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 07:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa30cc2f1e71cfb94dce8deacd45b0a763546952c48b7e260d525ebdf7f98f9`  
		Last Modified: Thu, 19 Dec 2019 07:43:02 GMT  
		Size: 7.3 MB (7324647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3faf523afedc85f30f0e1e3434153106f2696d7beb4c0ae0e636274e2a71d658`  
		Last Modified: Thu, 19 Dec 2019 07:43:16 GMT  
		Size: 41.8 MB (41844502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d53519d7691337589509cc5acdb604f462a7de4da274446bc569929379748c22
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83124560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e102fb2874ce523947bc171bee022da4907f56dbd5992f3d1781b6608816a30f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:55:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:55:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 07:56:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675452a43afa9a324be8e33f1aee9a8422bbced44f19139b1871a3eea6aaf06f`  
		Last Modified: Thu, 19 Dec 2019 08:04:31 GMT  
		Size: 6.2 MB (6175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca9b6ffa64dfd5bd3f2df67f78bab9050f47bc52390754a21794181e8485c29`  
		Last Modified: Thu, 19 Dec 2019 08:04:52 GMT  
		Size: 38.1 MB (38115797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d15c9cabaf5f3a398462eaad31d7b93997e35b091b6018002e4f91da4809d030
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86020683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6edc25bb482425db65167c2bbfb0f35afa0e93d4cd47f8619abdbb029da15b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:24:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 08:25:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3e85aa412983678f4d79eab41183f301230c76cabbeec30f45a51bf6506a9`  
		Last Modified: Thu, 19 Dec 2019 08:34:02 GMT  
		Size: 6.4 MB (6382300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5492d9cbad1ac41648538a34d8318c4aa70f18974db35adb3d86321a5b835bb`  
		Last Modified: Thu, 19 Dec 2019 08:34:23 GMT  
		Size: 39.8 MB (39761497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f5b32e352cbb71abf361fdea2cc4d719270154a6b30a6e5897b4f2768881faa2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94418044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dd8323c0c9a0bf02f20555eb1aa844158ab0689ebabec04020033d8cd30c87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:42:36 GMT
ADD file:cda22edb2102566fbf3f86c1dafef6df7ffe50c9b11154a3d86f026acea69884 in / 
# Thu, 19 Dec 2019 04:42:37 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:42:38 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:42:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:42:39 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:29:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:29:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 07:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e373c27c4badc3e1ae61907149678c5616314bf8094d3547bf7662744fb3aaf7`  
		Last Modified: Mon, 16 Dec 2019 15:43:11 GMT  
		Size: 44.1 MB (44110242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8b32694b976a17980d6cefad18f60834afa68f9ce12a392b255212740253cf`  
		Last Modified: Thu, 19 Dec 2019 04:44:07 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f78b1f7d4360832fe4f44a3caa2f66d3b454e00aa33f9b5e84c888dba46f13`  
		Last Modified: Thu, 19 Dec 2019 04:44:08 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c4ee9e5b6002551cfae8cca273105a1e765c986494d1b56bd813a855b72661`  
		Last Modified: Thu, 19 Dec 2019 04:44:07 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3897b6110e084ba8927e6b35bd2bea95fb3120d0df234f13e73f3edcea8f3a9c`  
		Last Modified: Thu, 19 Dec 2019 07:36:27 GMT  
		Size: 7.5 MB (7470115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86b64d74641c8214fcdbf51e661ebd62fb07786ef7a4f914f2299d6997f1091`  
		Last Modified: Thu, 19 Dec 2019 07:36:47 GMT  
		Size: 42.8 MB (42836157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7d5346952dcf05ff75a9b8556433a1dcebd7a6caebdfa31c46b60f71e3050d7a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98505865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de20fe0b9041f3bbb498f54d2e1dfdd9f12a603ae4cf784ae2b5c2d4587b0204`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Nov 2019 00:33:32 GMT
ADD file:251e99ab972ea3a03b4a9cb5a6a666707f4aaa78f9cf983e0b47203406a659f2 in / 
# Wed, 27 Nov 2019 00:33:37 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:33:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:33:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:33:48 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 01:00:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 01:00:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 27 Nov 2019 01:02:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a2b4c5f7bd29ff0e729d315a3429562a2a0fa4a2fad10c2b3cddc1024ee1f5f`  
		Last Modified: Mon, 11 Nov 2019 15:39:18 GMT  
		Size: 46.1 MB (46141097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4696d293ef28c197dc5fabb1bdba39a7b33c192ba7bb391f3b7a21dcbffcb5`  
		Last Modified: Wed, 27 Nov 2019 00:35:04 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210b001e0fc31a2c4813e1bbf67779dc31553f3a313dc37a600dceaa94b7d99`  
		Last Modified: Wed, 27 Nov 2019 00:35:03 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4264df61e52732869898d42e379df2d82b65739a66e2ff99653b170fe8b0f5b0`  
		Last Modified: Wed, 27 Nov 2019 00:35:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdb33f97c61081588d620a5ab68012ecca1d96f9b29be83c3ddc859833accd7`  
		Last Modified: Wed, 27 Nov 2019 01:12:46 GMT  
		Size: 7.2 MB (7233996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948f11785a6e3add56d28219d1138e123e6e96b1c631d1b50c3d160d6fc066b5`  
		Last Modified: Wed, 27 Nov 2019 01:13:18 GMT  
		Size: 45.1 MB (45129275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5ae82efb7ca77feab3dc99b73aac4509a04f609aa5d6b239a49a1993583f34c9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92462072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106fe52834c022437c7d62fdae4d0bc8d153b313dd6f9a6c922626edbe782984`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 01:19:37 GMT
ADD file:8286e4fedf1eced70b4221efcd13c80785dc092e26aa8ccade9dbe1226809b7b in / 
# Thu, 19 Dec 2019 01:19:38 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 01:19:38 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 01:19:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 01:19:39 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 01:55:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 01:55:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Dec 2019 01:56:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48f51d70b8a4133bccee46a02aa349e67904ed3f24c2fb97bfb473db957b8a57`  
		Last Modified: Mon, 16 Dec 2019 15:45:07 GMT  
		Size: 42.8 MB (42755727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0df1d6223b9644b62585bca4919334b4a907556e7dce45709a9fed74f3ccdb1`  
		Last Modified: Thu, 19 Dec 2019 01:20:33 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06865fc8b16c5e261c224fe334e7963414ee6bf96b9155660b22530e67e6e7ec`  
		Last Modified: Thu, 19 Dec 2019 01:20:33 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4565ea146d9a9dfc27ef0836a2c32882d4e20157894d4536c28936956ce16`  
		Last Modified: Thu, 19 Dec 2019 01:20:33 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640c69310f3824e7a7d211c70895e365b303c938443f0c48c36dbf77144375fb`  
		Last Modified: Thu, 19 Dec 2019 02:00:27 GMT  
		Size: 7.1 MB (7061214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe996693161ca493d79f2957adc6189cede56f9df1118024bf982a25699f949`  
		Last Modified: Thu, 19 Dec 2019 02:00:41 GMT  
		Size: 42.6 MB (42643645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
