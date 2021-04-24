## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:d4c28a6d645289f0c85806571305a4c2075654c6d8ef06d10ff71f49f3232242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:f7272f5b77380fe8a62cc8c5973b1bf0d16e9fa05f6ac09feba9eea876146181
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371784638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c620e2675fd51fec05e730679714d2a9aefef1d6d9a6a22423f0a39a49c20a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:11:43 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Fri, 23 Apr 2021 23:12:01 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:12:02 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:13:23 GMT
ARG CB_VERSION=6.6.0
# Fri, 23 Apr 2021 23:13:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Fri, 23 Apr 2021 23:13:23 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb
# Fri, 23 Apr 2021 23:13:24 GMT
ARG CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e
# Fri, 23 Apr 2021 23:13:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:13:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:14:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:14:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:14:05 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:14:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:14:07 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:14:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:14:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:14:09 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:14:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:14:10 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:14:10 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:14:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40c513b90a3a5bcb7f5f15dc2a983554305d585d944578130e03108493148bc`  
		Last Modified: Fri, 23 Apr 2021 23:18:43 GMT  
		Size: 5.8 MB (5833752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e71050d3c5a966db9ecc6b47d00497be9653126f5a68fa3bba239777645d9cd`  
		Last Modified: Fri, 23 Apr 2021 23:20:23 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277f962a6fd2888cecb621e1f65ddfa3bcff8d9e1ada3868ea971e15a0ccc95d`  
		Last Modified: Fri, 23 Apr 2021 23:21:00 GMT  
		Size: 319.6 MB (319572391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360e22a797af328303ed9330893654904b2de46fb14095d509dc6d641e7c2d70`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ed95631df30774f65adf8186ca57e5917c7a6971f80ee7a30309ae760a61bf`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3648db6783cceb36aebbccecd78c25b389b92c37a06ddd9bcf321c963664ad52`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95faa32d637551df83d7e37490362422bc3fe3f96b807f7cdd22a1dbd8e532e`  
		Last Modified: Fri, 23 Apr 2021 23:20:20 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e72b9534929ec3aa6c2f8c8a758f8de389cfb9519463ee37c158a87950d8295`  
		Last Modified: Fri, 23 Apr 2021 23:20:17 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c421270be8bf2f15635de7df8ce025e5d5ee58874ec810f8d0fbeaa5b0020244`  
		Last Modified: Fri, 23 Apr 2021 23:20:17 GMT  
		Size: 118.1 KB (118074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee07800f881b4331b170827f3410222a3c9a2848e16ebb799b3cf98a0b98d853`  
		Last Modified: Fri, 23 Apr 2021 23:20:17 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
