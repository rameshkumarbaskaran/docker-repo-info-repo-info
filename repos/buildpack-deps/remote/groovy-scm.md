## `buildpack-deps:groovy-scm`

```console
$ docker pull buildpack-deps@sha256:54d2d749de8f83ff35ea59fcadd18baad0243ccdf175812151cc3e5d41da9957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e92077f4eee25221cf7cf1e2571fcfb97039f1d622b37895462290a969ae1fc6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100818296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0150255a080b938ca092c70e0c1bf7b88b6c7dd3befeeb004d24f26cd0746b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:40 GMT
ADD file:eb088d03d9872f2347c5cb405459db6a9e8b6d43c043f0ab523769f08f1375af in / 
# Mon, 06 Jul 2020 21:56:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:43 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:20:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 23:20:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 06 Jul 2020 23:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:629a9a56ab697fab7c771f090bd2415d076bc2318eceb775bba7dbdf0551e62b`  
		Last Modified: Mon, 06 Jul 2020 15:50:25 GMT  
		Size: 28.4 MB (28371293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c43f8b7aaa9de0cef4278e06b17666b6b87b0e7bb59c54aae06046cbdb9d075`  
		Last Modified: Mon, 06 Jul 2020 21:57:37 GMT  
		Size: 31.8 KB (31829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ea68a6bcc0999d07e3eaa46659dbe5c06ab34220a758bede65242973a14b8a`  
		Last Modified: Mon, 06 Jul 2020 21:57:37 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859bf9b8406990fef5c0f0ea2336f51863879e72cd4aba1b00bc4e39f98637fa`  
		Last Modified: Mon, 06 Jul 2020 21:57:37 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b815fdd9b96bbe227931b9581b6dad75ce788a9e2468c255139579ef22343c2`  
		Last Modified: Mon, 06 Jul 2020 23:28:10 GMT  
		Size: 6.9 MB (6857960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7675a0b0a0306d87332bd68419600edc7a1c16c580ffacbe5afff7a2f4db95`  
		Last Modified: Mon, 06 Jul 2020 23:28:09 GMT  
		Size: 3.6 MB (3586649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786a6cbb317b7fab4158e10c63e96198079fc64d0520f4dacfca36e89fb14f08`  
		Last Modified: Mon, 06 Jul 2020 23:28:26 GMT  
		Size: 62.0 MB (61969556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d71a7917612e5850ffae6d4f10ce37556949606eb800a37b74a4208b818cb50b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99356804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6905cc36f689d6dc4afd46edaf0297e50a43a180c16e5536d2d8f182fcdc42f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:50 GMT
ADD file:35b0d977e8fc4305b3f988e3af2c52419e39aae68287af590636dfdb7487dbed in / 
# Mon, 06 Jul 2020 22:05:53 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:57 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:58 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 22:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 22:58:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 06 Jul 2020 22:59:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bca3f99199d9260076c548f38af71788f901900c99316e357c1dfb0e06fafbd6`  
		Last Modified: Mon, 06 Jul 2020 15:50:50 GMT  
		Size: 27.0 MB (26969246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf01b6284862c6caa2ce0e716ddb00705d21bb4f7cc4501c1fdf1130c17ffa7`  
		Last Modified: Mon, 06 Jul 2020 22:07:25 GMT  
		Size: 31.8 KB (31830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e991f38a848885cf9ff0e35cb51871c37ee33387f3159b4dbd1fa25146a3ecb`  
		Last Modified: Mon, 06 Jul 2020 22:07:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b128a6106c13f4424dcc44fef4eaa219acaf5f3c8510660e77bd90c81e6227`  
		Last Modified: Mon, 06 Jul 2020 22:07:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac980152f16f03da3b03b8a6b0804bce8a1c28151d843524b791230e868b1b14`  
		Last Modified: Mon, 06 Jul 2020 23:08:19 GMT  
		Size: 6.7 MB (6722628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d85f32459c314182a20d3c5effc3b5a3e1d981ed5cc5a38d6d9d1a22a68642`  
		Last Modified: Mon, 06 Jul 2020 23:08:19 GMT  
		Size: 3.6 MB (3570275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6337ecac2f2b8ff3b2253c1e677ba4d09ec9d9f8abf72bcff4ef2fffba92c328`  
		Last Modified: Mon, 06 Jul 2020 23:08:43 GMT  
		Size: 62.1 MB (62061790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f348fef63d08972ed7c9672b965a96c6fe1a20f59ce6a03494f34227c5b0cac1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116371946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e0fb53fb1d0d1fe60f86deda773a9610db62e4d0436248c630931396dc9eab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:26:10 GMT
ADD file:29a6559bb2b42840ad4a326cb87ec57e3d7acff070142d3c445e95a498608e9d in / 
# Wed, 17 Jun 2020 01:26:27 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:26:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:26:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:26:47 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:49:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:49:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:52:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b25075d60966612c3c64d57b4795ad61c96f1b6726b5f4e2bbe9895da022ab69`  
		Last Modified: Mon, 15 Jun 2020 15:49:24 GMT  
		Size: 32.8 MB (32831214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3ca039867a3a4d1f0bdce8cd95a4d5cae3bf26445e7da18368ea1a321552ef`  
		Last Modified: Wed, 17 Jun 2020 01:29:17 GMT  
		Size: 31.6 KB (31650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74cdff241e2c333351680e082de3609a7cbaaf2ad00a453b5b11f5d36990e02`  
		Last Modified: Wed, 17 Jun 2020 01:29:18 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9272e5603032808e3b694ab411de4202c12aa58e48b2e449ae98b88773a4684c`  
		Last Modified: Wed, 17 Jun 2020 01:29:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727bc1b8e91666a8974c3b58eec9076ddc3b3a8f1bf6fda0bedb6064373e2d70`  
		Last Modified: Wed, 17 Jun 2020 03:22:28 GMT  
		Size: 7.8 MB (7812013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed55ac2d20649312273a481dfa5a2c4d4577a25c3d297ac000ab717ccab6d14c`  
		Last Modified: Wed, 17 Jun 2020 03:22:25 GMT  
		Size: 4.4 MB (4447156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16157efe988f9cbb1e8d98aef1dda73691c6630e9365025c404156972b4ed9`  
		Last Modified: Wed, 17 Jun 2020 03:22:54 GMT  
		Size: 71.2 MB (71248873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:200fc934929b365501e806e995e9b31f505687b3546530f3719f3c3ad4b59742
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99031351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e6dc1cf8e090f34d5be1a79c717af6c9232b3e5b0a398c4933900a67c8f736`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 06 Jul 2020 20:20:33 GMT
ADD file:7c5297f390515aab00f66f663182cadbb3c5dbf52fb015526b80806df21de69d in / 
# Mon, 06 Jul 2020 20:20:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 20:20:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 20:20:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 20:20:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 20:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 20:46:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 06 Jul 2020 20:46:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c5e60e47f65a4306c7d2ad46d35b9ea6d4aaf9cb77add2bff5be52a742d23e4`  
		Last Modified: Mon, 06 Jul 2020 15:52:10 GMT  
		Size: 27.2 MB (27174117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6ddf166e3f11601f2466edd2cfbfe9942c0f85314ffb2ea31f66bb6d0cf123`  
		Last Modified: Mon, 06 Jul 2020 20:21:35 GMT  
		Size: 32.5 KB (32456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076f8572b34a88b603a66fc9eba9b5237c09e64670ac0d8a02e024d6e3ade52f`  
		Last Modified: Mon, 06 Jul 2020 20:21:35 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f928d1948ab604aafd2985aaa9196351c03043dee8e4bbbd73f4cbf190abb675`  
		Last Modified: Mon, 06 Jul 2020 20:21:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11eec02dfd95f6d6df751544a08b98b891c24c0ad561386ffd22b32592094376`  
		Last Modified: Mon, 06 Jul 2020 20:51:12 GMT  
		Size: 6.5 MB (6545554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a9f1cd556b3c6d476e9540bdaec30b426c7e295beb757e67cbbb2a3bcfc3ca`  
		Last Modified: Mon, 06 Jul 2020 20:51:17 GMT  
		Size: 3.6 MB (3579909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4fdf7b85c7ed6238d1f8fd569fe19a41f284dcbd0bafb9e99a4684406a54758`  
		Last Modified: Mon, 06 Jul 2020 20:51:31 GMT  
		Size: 61.7 MB (61698287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
