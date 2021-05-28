## `buildpack-deps:groovy-curl`

```console
$ docker pull buildpack-deps@sha256:a6a98bb42817f47cfa48c971f8e5f159eb56f94daa463a7143abd5557b77d0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:02f9efaad7a432dfc4a91785ab2fdf42c6bc990a5598aee77988ec60d77e070d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40407719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612c7ca15a209fe45e6c0d96b5b7b172216838c564e1679f9a8f0decea96ae10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 May 2021 00:28:11 GMT
ADD file:5582a76cd73639bd7b5f941762801034fe6d3297d63d8333085c79c31b5e777a in / 
# Wed, 26 May 2021 00:28:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 00:28:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 00:28:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 00:28:15 GMT
CMD ["/bin/bash"]
# Wed, 26 May 2021 00:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 00:49:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0dfa4d6d32846900cdf518b31b7420c8e3bee78df56f061347f079b085e55eed`  
		Last Modified: Wed, 26 May 2021 00:29:22 GMT  
		Size: 31.3 MB (31339605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ba66a34e9b2cf96e7958749a4fdd29a90699b6cd7eb67976c266a8277a26b`  
		Last Modified: Wed, 26 May 2021 00:29:18 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6382425bb0d013b4122cc28ffc63f8bce680a6562260cb6fa715f6f16a59db`  
		Last Modified: Wed, 26 May 2021 00:29:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2855a438bbdf35b205c11cda343e79b366b32de44c66547fce2c6eef2ef7687b`  
		Last Modified: Wed, 26 May 2021 00:55:21 GMT  
		Size: 5.4 MB (5404036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c480a4de53ba6cd27f663db2d65a56c0919c0842d6b514480024ac528f40ea4b`  
		Last Modified: Wed, 26 May 2021 00:55:21 GMT  
		Size: 3.7 MB (3663044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d9aad866ea1ef1b50a53a1a4cc7a54c6a1a4735ecc9e2ea7a5521638f4e400ab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34294626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9156230c4ce0dfc98f6e4521849b062c26b7b79171672fd531ad7e38e7047c96`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 May 2021 17:00:48 GMT
ADD file:64ff5c201737094749a157eeb3e4907949b36f17c0e8c4d4b2b7ac9633fe776c in / 
# Wed, 26 May 2021 17:00:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 17:00:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 17:00:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 17:00:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:53:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0e120224dfb47b00043c7e4077e526b2e311c86bb064631d6405bd428892c3c4`  
		Last Modified: Wed, 26 May 2021 17:03:50 GMT  
		Size: 26.3 MB (26313179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c256fbca870ac2acbc49bfa8e307393013f9593e0623e4ce9b0fd12c73c61c7`  
		Last Modified: Wed, 26 May 2021 17:03:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78179aa140f91b4c62e4a8a0c00c0f80a39f112b766c4e88be615f421c9d13d9`  
		Last Modified: Wed, 26 May 2021 17:03:45 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c31b2d3a6bdd8d0276daceeeb3d1cdc698234eb896fc1a371ec2c72d5a2ec2f`  
		Last Modified: Thu, 27 May 2021 01:11:43 GMT  
		Size: 4.8 MB (4840293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e366c83e8a1f0d1255ddaa8ddc08b77b5b167f35e730ab61d4847ccf2b6a1d`  
		Last Modified: Thu, 27 May 2021 01:11:42 GMT  
		Size: 3.1 MB (3140115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:92a50cf1ff767f6c51036b42e3573d6d86d743d90c77dbee70c1cb3f22e133b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38883086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb09674bcd2fd52dc4708c28ff510243ab1276c63dbbe2c6e02dbaec13f36e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 May 2021 12:30:07 GMT
ADD file:9f38584e54932330e111128e5969008e1d92aa7ee1b7f3af0622ee11a30ef661 in / 
# Thu, 27 May 2021 12:30:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:30:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:09 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:59:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:67cef43ca337885b5e8a4dc8a670b30651b42874b8fcf384957f2b016bbee3b7`  
		Last Modified: Thu, 27 May 2021 12:32:19 GMT  
		Size: 29.9 MB (29875040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93db328fd29467d3c5333c2f202b25c4d50c45cb5980d8f02fea273bb32bf310`  
		Last Modified: Thu, 27 May 2021 12:32:15 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4818fcf480a4c3442f1bf3dfb05adec183af6b462b89783fa8ad4c8493cd8746`  
		Last Modified: Thu, 27 May 2021 12:32:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296ddaeecce03790530b283e70ec6fe9c5132e608d6b3d208de7adb676d0b7ca`  
		Last Modified: Thu, 27 May 2021 21:11:38 GMT  
		Size: 5.4 MB (5372324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d297176d9ea581c24c19136bb30f276c603bbccba48803760cf2935aa5b318`  
		Last Modified: Thu, 27 May 2021 21:11:37 GMT  
		Size: 3.6 MB (3634689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d9e6d6022c92604ed9a28b4b64527d2166016b1662f2b0b087b12883b93fcd66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47108693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5fa9d93b1cb33dab02a536a137c9bfa8344af046edc5ad64bb2b2e77e0c37`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 May 2021 00:50:59 GMT
ADD file:417e85e230e48984b1cc0db245a092e51901fd8cf010070a82fd06ccaec211df in / 
# Wed, 26 May 2021 00:51:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 00:51:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 00:51:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 00:51:36 GMT
CMD ["/bin/bash"]
# Wed, 26 May 2021 01:12:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 01:14:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f7501b08507a493babfe9a7a361950a90febd51f598365c8c72a27438e176910`  
		Last Modified: Wed, 26 May 2021 00:54:09 GMT  
		Size: 36.5 MB (36545421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039b1bdfb29d855647202d2d86b6473a9b637d7edaafa7d199fe951071b946c0`  
		Last Modified: Wed, 26 May 2021 00:54:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63192a9aec9ad98562f0c79212fe107a71c90d1b3f55488cb16ca414d1d6853f`  
		Last Modified: Wed, 26 May 2021 00:54:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296ee47b5f35b125a133ce4bff94c000b52b76e704739c5a0d46be38f7deca42`  
		Last Modified: Wed, 26 May 2021 01:40:49 GMT  
		Size: 6.0 MB (6040577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfe4cc2db417d1a39f70a65a7e940e02096578289517774312678ebf9ab77b2`  
		Last Modified: Wed, 26 May 2021 01:40:49 GMT  
		Size: 4.5 MB (4521657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cd1e51f2135d90d6e92dad8d1c8fcdb1d1e0cc4faf54c64c18e61bbebb264b63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41350837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d20d95d19b82b98c0789696536c9c792712e833df25378d0ed89ba662cbf463`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 May 2021 00:50:49 GMT
ADD file:953040401ce401194c7939af20d4b65872f29c9f1c9e9411f5b04fbd299161d6 in / 
# Wed, 26 May 2021 00:50:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 00:50:55 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 00:50:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 00:50:56 GMT
CMD ["/bin/bash"]
# Wed, 26 May 2021 01:14:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 01:14:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a86f368f271868bec872a3e420550decf4fa2f153ca0ebcec9ab48b642f129b1`  
		Last Modified: Wed, 26 May 2021 00:52:15 GMT  
		Size: 31.6 MB (31563545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf527448b6952fd5c7da27d42ed151c11bafb569d579a96ce879307419f0970`  
		Last Modified: Wed, 26 May 2021 00:52:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d46e2e6002b01a57ea745988830c3950a2aa33250abe3ebcd67891351feba1f`  
		Last Modified: Wed, 26 May 2021 00:52:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039f58efad91acfba39b19901da37ac258ccb25fb301301dfd989ca742b01940`  
		Last Modified: Wed, 26 May 2021 01:19:29 GMT  
		Size: 5.6 MB (5629719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294f314beb8886b2a3ca040687069cef7b938d4da9642e8ebc5ca6d4f575bf2d`  
		Last Modified: Wed, 26 May 2021 01:19:29 GMT  
		Size: 4.2 MB (4156537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
