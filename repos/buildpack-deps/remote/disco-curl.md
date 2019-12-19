## `buildpack-deps:disco-curl`

```console
$ docker pull buildpack-deps@sha256:06413436f7bfbecda19ded4c20b629c7b8abc1aca9b7653c7a0d19801a140de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:disco-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:317c7e2b1beda1963905ea3823b01c9db710c5c986a28834bde59724d9e175e7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37846658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd0e0da11b4ad2bc7ca27d2e745f03716a6d04418908405e986723f306f113b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:22:14 GMT
ADD file:440e68453fcfc383ab4ed0339f77dd56451b14f52cab4ee1e209062af03d5042 in / 
# Thu, 19 Dec 2019 04:22:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:22:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:22:16 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:22:17 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:25:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:25:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3e6c0c31900e0291814a94e9e8fe953d329b8f9f6a426659a45d7c05e08db089`  
		Last Modified: Thu, 28 Nov 2019 16:25:20 GMT  
		Size: 27.6 MB (27621412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b269ca9077748a3ef472411d5485716d58776f6e0635daa39d51bab4c48ca33`  
		Last Modified: Thu, 19 Dec 2019 04:25:06 GMT  
		Size: 31.0 KB (30991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78aeffdd139d0483a89257110baafbfa91ee684dca0bd8c30a4417cccf92f5b7`  
		Last Modified: Thu, 19 Dec 2019 04:25:05 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f2067539ba72f36bea210a390bcda78f3df29cc30b9e2b0dd69659ad579248`  
		Last Modified: Thu, 19 Dec 2019 04:25:05 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0621f3a9b9391f4bb6ec41d81eb260043bc789af61367922cec85c27c0650cf5`  
		Last Modified: Thu, 19 Dec 2019 07:40:09 GMT  
		Size: 6.7 MB (6678575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f457e320fd24a14498c03b68333f4c74dd616154bbbfe95788524b88db1043f7`  
		Last Modified: Thu, 19 Dec 2019 07:40:09 GMT  
		Size: 3.5 MB (3514654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:disco-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c85d2b475add4856d35e1d9258f2ee3e3adbddddc1d601f854cdbec6fe226cc6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31776555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46d375312e4326b49a5288043388a1a16f73287008407eea0c36b739adcd227`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:10:06 GMT
ADD file:f9669865ddc50bb8650af3ed6c57646adafe85c0eabab5873d8a9e535d3cb49d in / 
# Thu, 19 Dec 2019 06:10:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:10:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:10:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:10:29 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:43:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:43:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4a739c8de1a69ff64de6b100dc29743b69430003f16ef12e7853a0be38137d67`  
		Last Modified: Thu, 28 Nov 2019 16:41:44 GMT  
		Size: 23.1 MB (23115784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab10507a1d4316077c17726009f626443411c4ff7bc3b642cbdaf65e6382f2bb`  
		Last Modified: Thu, 19 Dec 2019 06:14:57 GMT  
		Size: 30.9 KB (30949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf56d4bab227accb0531ebfeb8a02b247f3f52af96ead2360fffe4402b24e9cc`  
		Last Modified: Thu, 19 Dec 2019 06:14:57 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a26640da9566e71958759ca420a603fed375d152ffbb648cd9f587dc3ce904`  
		Last Modified: Thu, 19 Dec 2019 06:14:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d4a25220b9e9e37902e03730d80db9f3339ffcd464ac00a241e790e3d36f33`  
		Last Modified: Thu, 19 Dec 2019 08:00:20 GMT  
		Size: 5.6 MB (5649862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36c2b4747023bde64cf789e14e82f0df5a36cff597aaa3d758fca0726425db3`  
		Last Modified: Thu, 19 Dec 2019 08:00:19 GMT  
		Size: 3.0 MB (2978904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:disco-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:88f4fa4e98f24d82508171716c738fec5f24ab46762c8a52c21ba1325a68d3b1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36468397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9794c772a83359ce9e1edfff8cba19e964c5b94a8a7fe730183bdbd9748fbcce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:50:57 GMT
ADD file:74f072c21abc354f4180a342a84c4a92bd67887a975e13515af0e727fa871c1e in / 
# Thu, 19 Dec 2019 03:51:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:51:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:51:40 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:51:44 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:13:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:274e1e3371b9df5253f5129528edfcf609063a8cece74211061e6043da68ae53`  
		Last Modified: Thu, 28 Nov 2019 16:38:51 GMT  
		Size: 26.4 MB (26379071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6467cc73172e25ea7ce12129305cd7fc00af3ccb8176c4345c968d8d449b3b`  
		Last Modified: Thu, 19 Dec 2019 03:55:56 GMT  
		Size: 30.8 KB (30788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac06a88f4c8b446cba8f3dfac10f2a041fb9255d820ada2579734dafef65025`  
		Last Modified: Thu, 19 Dec 2019 03:55:56 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3142f8a3358dc0b8523d6d567aa4078b40eb2debe886fd45844831852892cd46`  
		Last Modified: Thu, 19 Dec 2019 03:55:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a06dc5e0969290195ec067db1570c19e53225637bd7e23481b08fbbc0ef0d1`  
		Last Modified: Thu, 19 Dec 2019 08:29:58 GMT  
		Size: 6.5 MB (6548494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60ab4e4a03908816c18a914e659ee84b6c541c606505a6c5f803ce479e5e25`  
		Last Modified: Thu, 19 Dec 2019 08:29:58 GMT  
		Size: 3.5 MB (3508992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:disco-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2c79a92db8beacbe761650bf92a1548e7b175cbcb02f59b436ef39673695eaae
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39113795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1046d6f6aea986aa2cbc696a7387b9aa4bb79b50dd710b561d28e016c2d292`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:41:22 GMT
ADD file:90c4f412a27377450f42f959a8499369f4f6c4e8cff8f6c29d6617efc16846d7 in / 
# Thu, 19 Dec 2019 04:41:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:41:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:41:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:41:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:20:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:21:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:376760364fced29d0393f7886dc15d2a26859f4c46b1d63f042889335bd71e52`  
		Last Modified: Thu, 28 Nov 2019 16:33:54 GMT  
		Size: 28.3 MB (28284941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9465e57adc8332b9ca50490b50abf1d2b4af6d528b927c8ff360d9f2cb796e4`  
		Last Modified: Thu, 19 Dec 2019 04:43:04 GMT  
		Size: 30.3 KB (30255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23613330016823644dc6305147f1e47bc1f090e8b599820829eeceb9ddf1c95`  
		Last Modified: Thu, 19 Dec 2019 04:43:04 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e33bbc3db68932b6d76a343a293072eff9c635e33ef363cb1e1943596d737c2`  
		Last Modified: Thu, 19 Dec 2019 04:43:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d14ec06ef34500059d48ad7d054ea4283b22592bb766a20374751972186a295`  
		Last Modified: Thu, 19 Dec 2019 07:33:59 GMT  
		Size: 7.0 MB (6990075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32019a8d05b3d39dfd93da87b203dcaca547accf7a8fbdc0e73ee9973be3da1c`  
		Last Modified: Thu, 19 Dec 2019 07:33:58 GMT  
		Size: 3.8 MB (3807498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:disco-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8c9429dc02b3d92b16cafb4e6a61107ebaf5c1bb8a4e36232fd145b8acf6e8c6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45129188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5494c530acc98352756d86d6f76d80f93e8143f0a56d7c6d202eb72d559f54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:53 GMT
ADD file:1eaaab578f92615bf7919345bff4e3eaf8bbf00322a7ef77a8ebb2c44c945da7 in / 
# Thu, 31 Oct 2019 22:21:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:21:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:21:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:21:14 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:32:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:33:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7e97fd59dc6426eb90f9a2c13735cf6e69fdd3784d9729c95b6b6af920b151cd`  
		Last Modified: Thu, 31 Oct 2019 22:23:32 GMT  
		Size: 32.9 MB (32882160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a939319a7332feeb5182ea58c1152de415002b52fd86582d2747281fdf82ab2`  
		Last Modified: Thu, 31 Oct 2019 22:23:25 GMT  
		Size: 30.8 KB (30812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf0389cd600ed2b74837013b0f9e56ed6d8c171d807796c48013c2dff990a26`  
		Last Modified: Thu, 31 Oct 2019 22:23:25 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d678865ff31acd1d617068b9a82621ad0e51a7f2a563bc1a7141f5f155441271`  
		Last Modified: Thu, 31 Oct 2019 22:23:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeee6882148ffba34e73f9605e31769c96d56f3ac3814cdf6752314045b40945`  
		Last Modified: Thu, 31 Oct 2019 23:50:20 GMT  
		Size: 7.8 MB (7750770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e0f87c1f237a5396da350370be9a75259111bfeb801f8292c07133cf9c3583`  
		Last Modified: Thu, 31 Oct 2019 23:50:19 GMT  
		Size: 4.5 MB (4464391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:disco-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c7b1b69340e5fc867404b5aed4858379c1d200e4ae0af6ba88f07f469a1c007b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35894458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1388c8f1dd4b5d973c020fbd918861f68a91fdea3ddc5b4596a8fe9cfbcc296c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Dec 2019 01:19:04 GMT
ADD file:e1eab19f8266231e5e877ec5fc87f33c44e22a25e663c53dcee20b24f34609ea in / 
# Thu, 19 Dec 2019 01:19:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 01:19:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 01:19:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 01:19:06 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 01:49:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 01:49:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5c2a33b5686f7a11b05aef16500d862ac9177c4c5e5ad056110a09e0691a20ea`  
		Last Modified: Mon, 02 Dec 2019 15:34:45 GMT  
		Size: 26.2 MB (26202792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f5a2b58f565be04e2a94ff13238660cd2fe0b63812fb0b2427b844eafabce2`  
		Last Modified: Thu, 19 Dec 2019 01:20:01 GMT  
		Size: 31.6 KB (31571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6329b5fdb30251895f4bb6e7c1bf7f31c314068ba9f64b6143def9c5afb1094d`  
		Last Modified: Thu, 19 Dec 2019 01:20:01 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57470f2255b0980c683b1dbddbcbbb40801b1e457eb5dd42bad160d87467c52d`  
		Last Modified: Thu, 19 Dec 2019 01:20:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48610b9e4fdfa5fc1f4275236f017eb0f2492e030ecbcdc9944937d71e4b2a97`  
		Last Modified: Thu, 19 Dec 2019 01:58:18 GMT  
		Size: 6.2 MB (6227095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943617e4153e0ba3cfc546097d675021e6031bfff01f971e3f882e34261d7558`  
		Last Modified: Thu, 19 Dec 2019 01:58:17 GMT  
		Size: 3.4 MB (3431978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
