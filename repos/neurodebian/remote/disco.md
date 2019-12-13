## `neurodebian:disco`

```console
$ docker pull neurodebian@sha256:795b8943a41a3ae3c1c58c8232da973855db3284dfbf838269cb5c7315186424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:disco` - linux; amd64

```console
$ docker pull neurodebian@sha256:2c4525f7fc79d095acadf3561b404064ab099412a0ad811bf371ae0715c28a39
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33307592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122ee3530ff9636e1f23f5ebea14a86e69417bfd9d061064a2726f1a58c58473`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:51 GMT
ADD file:f450b57fc821cd65bd59da8799f753e86ea8f3e5cd7cf0ede5e5512327aa61e1 in / 
# Thu, 31 Oct 2019 22:20:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:53 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2019 00:26:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Dec 2019 00:26:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 13 Dec 2019 00:26:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian disco main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel disco main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 13 Dec 2019 00:26:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b21821a6200724aba9a49fe310d920819975191082b845ee8e34c4871d92cdf4`  
		Last Modified: Thu, 31 Oct 2019 22:21:51 GMT  
		Size: 27.6 MB (27621247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3052859eed3080fc96b719cc8b6ac03bfef13e0bed65966773b6cdcb1374acf2`  
		Last Modified: Thu, 31 Oct 2019 22:21:47 GMT  
		Size: 31.0 KB (30988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba68c59156676c4890f34bb6f00da24441138a1053e6e85a3fcb448155058b8`  
		Last Modified: Thu, 31 Oct 2019 22:21:46 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab6656eb3a7c5333cc5c4aebc6bbdf3974563e5bbaa6809f3334f2ee6b1144e`  
		Last Modified: Thu, 31 Oct 2019 22:21:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a035e1c40d5ee17ce39d25851cce4e108a7851b83a243474a42c4d1bbb15cb`  
		Last Modified: Fri, 13 Dec 2019 00:28:07 GMT  
		Size: 5.4 MB (5418294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61849ab75d2467c3c29a2f7de69d3c041a45e224a524f4afbd65527efb953d4`  
		Last Modified: Fri, 13 Dec 2019 00:28:06 GMT  
		Size: 3.2 KB (3152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c7afe84f1a49a4817d8029b8515e0e54a741b88384a2fc52bf49505f761444`  
		Last Modified: Fri, 13 Dec 2019 00:28:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d73395d0698a9e9d2ccd938ab3f34493128b7b1ec9422dbe2ec2ba3852a72c`  
		Last Modified: Fri, 13 Dec 2019 00:28:06 GMT  
		Size: 232.6 KB (232644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
