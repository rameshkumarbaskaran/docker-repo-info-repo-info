## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:8751c72e9a5250c711e40d609f5f91bc59570ce154f0b255f4eab45af335eeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:caa5da5b014b06b18bf23b028a73807517a85d9f8de61034d7c72d7b1b68d056
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.9 MB (549932596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af423ed32e366e7cf4554784c3863bf39b5546caa9bd673f2a3dc688d0ec432`
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
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_VERSION=6.6.2
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2
# Fri, 23 Apr 2021 23:12:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb
# Fri, 23 Apr 2021 23:12:03 GMT
ARG CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901
# Fri, 23 Apr 2021 23:12:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:12:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:12:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:13:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:13:02 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:13:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:13:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:13:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:13:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=8ba53d979541aa2d4c1abc75919b2ff52cf90f40274f86b20fca31101faa7901 CB_VERSION=6.6.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:13:06 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:13:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:13:06 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:13:06 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:13:06 GMT
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
	-	`sha256:0c1f453513ef950ec91beaded0343dcdbf032b28aa40e82b0acd0bfbcfca7229`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fb83af01f8a94d408a24781f1c77890ce3fff5d62f1512dd0a5eded95c0482`  
		Last Modified: Fri, 23 Apr 2021 23:19:57 GMT  
		Size: 497.7 MB (497720349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6b306fdf033c4070487ea46043c7884bb67f35f6125808b47834fa4771912a`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df32a98f35e01a703925c7202ec8d663c6c84dfd0f0bf2d25501f241d26ff4`  
		Last Modified: Fri, 23 Apr 2021 23:18:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c397fed50d7adaeabe853c0644f5bf1b8b9aee9a73744bf4c3f3446eb4de4d`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a74dc1fcdd9c1c06dacbe6b522838b16947af175dee4a9fc91acfa7e0fc264`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61efea708740e1b858be2d6d65018fb662bf7d0eca6e5db534dff9f46d702661`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4638d2c9b6424e8f36a00e4f1f5fc4cad815c39f3c12d1f94d9b29dc799e6f`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 118.1 KB (118073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b028c8df2f893a44004f4e0c22630c0d9ff7563ff8669b49ab53762a29f842a`  
		Last Modified: Fri, 23 Apr 2021 23:18:38 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
