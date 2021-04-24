## `neurodebian:groovy-non-free`

```console
$ docker pull neurodebian@sha256:32e4e15c884f5b1665ebca65412f89fa496c5c116d84e6a1e89b0d2a0ebeba7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:groovy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ea7ae997dac568c8112bbe5a3f9beb34d2bbe657220b17920d973884fe87021c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37185209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ec780422d36976bb2afd863f81dd665ddfe9107e4065f13e174c2f15270bbb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:45 GMT
ADD file:49bbc9f3e694569cb33bd86c7b98d116c9a6401968af70ae5f2faa640a86ae4d in / 
# Fri, 23 Apr 2021 22:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:47 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:49 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:28:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:28:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 24 Apr 2021 00:28:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian groovy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel groovy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 24 Apr 2021 00:28:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:29:00 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:eed86eef5a4687135cb1ba7c55da6af79c9182e8bf59b53a880d1b334515c8e3`  
		Last Modified: Fri, 23 Apr 2021 22:23:28 GMT  
		Size: 31.3 MB (31329297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e7e9027772b319849250afcb0ac9b214cfd61a4ea65eef21001b65ec00e88d`  
		Last Modified: Fri, 23 Apr 2021 22:23:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b553362680befa8cc008aea80bf47a5d16e8d2ed9ffc4287ddb0775a434b69e`  
		Last Modified: Fri, 23 Apr 2021 22:23:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7164f55c99b2fedbf8740d071488ab52e1c82eed971fc480256e49ddbe4e6826`  
		Last Modified: Sat, 24 Apr 2021 00:31:14 GMT  
		Size: 5.6 MB (5596810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f937e51d77c940b3aa591d7e633c78f686ad389cd97e79a69c7fa36aa504a1c4`  
		Last Modified: Sat, 24 Apr 2021 00:31:13 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666df9820510829c960eab2194574e5229146f94116bbf044c2990de03fcfcf8`  
		Last Modified: Sat, 24 Apr 2021 00:31:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635d7fd5563b39c3064d7654c919aac03b493ceec330b8ecb6569075cec2a13c`  
		Last Modified: Sat, 24 Apr 2021 00:31:13 GMT  
		Size: 255.8 KB (255797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b06fe42ab3a9d3ffb3c71fd3e692081e5d2907c043a0336eef044395c5fc8c`  
		Last Modified: Sat, 24 Apr 2021 00:31:25 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
