## `couchbase:enterprise-6.6.0`

```console
$ docker pull couchbase@sha256:79c4f1e0c4e9f79f8d6946c1b3cef60626223ad5a40b9c7bb2d30c6018f4620b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:f7cbf2222a070142576ebd839a053be6c156970667f0b65ee38cffe2deac5255
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.3 MB (527317903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620936063bcbda07dad2eb967daca0c3124e6cc0651a33853ad38ff84d87c46c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:54:38 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:54:40 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_VERSION=6.6.0
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Thu, 17 Jun 2021 23:58:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb
# Thu, 17 Jun 2021 23:58:46 GMT
ARG CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728
# Thu, 17 Jun 2021 23:58:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:58:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:59:42 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:59:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:59:47 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:59:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:59:48 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:59:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:59:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:59:50 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:59:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:59:50 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:59:51 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:59:51 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f23c2914264c712559d0bcc77a85377f94c9649ea3235072b3662e5d72a8cbe`  
		Last Modified: Fri, 18 Jun 2021 00:12:30 GMT  
		Size: 7.4 MB (7373851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5425c7cb0264c4c96e1eeef15ff71e54279d96b92737fbf84031243f93ba6d1`  
		Last Modified: Fri, 18 Jun 2021 00:12:25 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c473aa431222137a0c0c31086a7eed2d2ef3b44970d0edd9aa178f0cb6749fad`  
		Last Modified: Fri, 18 Jun 2021 00:15:32 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b29e96ab7f88383ed71e42898311493724ecb11f4ac8bb2ac480f5fee2f945`  
		Last Modified: Fri, 18 Jun 2021 00:16:31 GMT  
		Size: 493.1 MB (493120683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead4ed436d77566312e872c28579ad4b0f6c1a60f23b22ee7bffa84344cb6dd5`  
		Last Modified: Fri, 18 Jun 2021 00:15:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff614568b5af842843683e3ec14347f4f78e3d51b6f536eca2779fcf53b24688`  
		Last Modified: Fri, 18 Jun 2021 00:15:32 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812cee8bf697619628847e394dde527001cd621075d30446fa41f6694a6dde31`  
		Last Modified: Fri, 18 Jun 2021 00:15:29 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569987df52c8083e8cebcb3953ba11ec4e46861309a34158714c09578f0d5d9`  
		Last Modified: Fri, 18 Jun 2021 00:15:30 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abb0766038a93cf47e1abc53d946272fe1634ce753eae46be98c4a6bffd5d2`  
		Last Modified: Fri, 18 Jun 2021 00:15:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7178ff9751618abb1f3fe07987c9631e5e8f9a3da9e4d9a8772faa8b945e225a`  
		Last Modified: Fri, 18 Jun 2021 00:15:30 GMT  
		Size: 118.2 KB (118186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18537c9ec688aac9d44245eef7385fe9aea862a27004c4fdce96aa1b7bf0357`  
		Last Modified: Fri, 18 Jun 2021 00:15:29 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
