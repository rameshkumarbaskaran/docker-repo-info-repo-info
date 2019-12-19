## `couchbase:community-6.0.0`

```console
$ docker pull couchbase@sha256:ef03c8abc25a8fbc08c00a94acc73f6263124be33a482d5891790a1918b4503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.0.0` - linux; amd64

```console
$ docker pull couchbase@sha256:117bb5abd494c81652affce51e6637a624db687fe85f471ea3f80f4b726331cd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199468336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508feb8c5fde2d369cf5c0509f83ec3401c09ba7b32f7b18c0b7501d6a87485`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

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
# Thu, 19 Dec 2019 06:36:40 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 19 Dec 2019 06:37:19 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_VERSION=6.0.0
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece
# Thu, 19 Dec 2019 06:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 19 Dec 2019 06:39:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 19 Dec 2019 06:40:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 19 Dec 2019 06:40:20 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 19 Dec 2019 06:40:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN chown -R couchbase:couchbase /etc/service
# Thu, 19 Dec 2019 06:40:21 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 19 Dec 2019 06:40:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 19 Dec 2019 06:40:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 19 Dec 2019 06:40:23 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 19 Dec 2019 06:40:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Dec 2019 06:40:23 GMT
CMD ["couchbase-server"]
# Thu, 19 Dec 2019 06:40:23 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 19 Dec 2019 06:40:23 GMT
VOLUME [/opt/couchbase/var]
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
	-	`sha256:e35cfbf2546f178acf65d54d00dea29c862a5aa1e13db5369ec2d40b471b6c54`  
		Last Modified: Thu, 19 Dec 2019 06:40:40 GMT  
		Size: 14.3 MB (14330783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dae530d69d4a12e6c0699565010595a4a5de7a53b335ad119985ad10c713ce`  
		Last Modified: Thu, 19 Dec 2019 06:42:49 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecaaae3a981119abe142b0d3d269226a30e92467e0cfeed4cd8fc18ba2fe5f9`  
		Last Modified: Thu, 19 Dec 2019 06:43:12 GMT  
		Size: 140.9 MB (140887945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fb5a83fffaa82b9702184605283f83589ae68264da669c883d4ef96a09289a`  
		Last Modified: Thu, 19 Dec 2019 06:42:48 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554c574542d7c7b93d9187a88ca9247c40a90a63237f5f1b58da1b08ab79471c`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f60c2c021044652e527645d4f3ee9b02c534fe8494bacfa50e566c3a476855f`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9c777ec4eb62d198feef0dde2f8505e537b3218b246d5d317c60f81bd1600`  
		Last Modified: Thu, 19 Dec 2019 06:42:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21135c2641aab927ccd79e3257ee46c01b5ec66242964512efb210e958d0a2`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d69977d46e6e54ee73a24cf959e755e5961ba5df292de9ee38f0995474abaf1`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
