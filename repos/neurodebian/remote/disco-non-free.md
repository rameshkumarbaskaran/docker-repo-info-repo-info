## `neurodebian:disco-non-free`

```console
$ docker pull neurodebian@sha256:72e8875eef846e8c95392cc5a753ef9cd73078ea04e5395732017cc19cba0e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:disco-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:62c16bcf18fc148237cf92cffef745f90cf9568800c6d665715d96fb9f5ea05f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33307652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72aca68e8d1d2b51b8c8bf070e582dd59bc60dd23b1c94d444d2e67a38238dd`
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
# Thu, 19 Dec 2019 07:49:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:50:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 19 Dec 2019 07:50:01 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian disco main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel disco main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 19 Dec 2019 07:50:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:50:13 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
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
	-	`sha256:be582cdab8036eddb8211a657f3c8dc1ccf565d70c5cf3298e6cb95b65f5fc33`  
		Last Modified: Thu, 19 Dec 2019 07:51:30 GMT  
		Size: 5.4 MB (5418102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bd21480dc3ccfece98765d21275ac06e705ebe3f337ed44655de8755e93e92`  
		Last Modified: Thu, 19 Dec 2019 07:51:29 GMT  
		Size: 3.2 KB (3151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d116dd2b44eef28d55ef23c6ec83674623a84fe5a2dd427ddd69f3a06aebad`  
		Last Modified: Thu, 19 Dec 2019 07:51:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a8439d5a3d3d1d93acd4a512beebef5fa95123ec21a6bf57a24f469b6edca5`  
		Last Modified: Thu, 19 Dec 2019 07:51:29 GMT  
		Size: 232.5 KB (232467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca1eea059255240ff0fbe2c18cd88808f6f0428890af6b76766f2b3de3a9ef2`  
		Last Modified: Thu, 19 Dec 2019 07:51:33 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
