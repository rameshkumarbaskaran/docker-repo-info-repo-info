## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:b5aea78e469e3a463087113d052534ee5ef020ba3e0f7dc3958ec97ce06533c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:f22333a187037afac2f54ab2684c847024f2a8fe2e881133548f7dc9e70e80b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132817765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdeb95960da51485e7d52c6bcb9cc1d05f67786c4d5cc5a5038bce724e3e0f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:19 GMT
ADD file:80aa4dde5bfd685e5e660dc6ff1db4713d69bacf53ff51b7e85f8fcff80513eb in / 
# Thu, 02 Dec 2021 02:50:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:45:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:45:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 04:12:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 03 Dec 2021 04:12:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 04:12:39 GMT
ENV KAPACITOR_VERSION=1.6.2
# Fri, 03 Dec 2021 04:12:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 04:12:45 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 03 Dec 2021 04:12:45 GMT
EXPOSE 9092
# Fri, 03 Dec 2021 04:12:46 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 03 Dec 2021 04:12:46 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 03 Dec 2021 04:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 04:12:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a44d60f8dd45ac8efc157e797930e23cf3e360bb4aae7c745efcb02c562c3e4c`  
		Last Modified: Thu, 02 Dec 2021 02:57:12 GMT  
		Size: 45.4 MB (45381394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6368c5e7052170a880eff5a8f1669746c215797100578cc50a2a4903aab88a0c`  
		Last Modified: Thu, 02 Dec 2021 03:53:06 GMT  
		Size: 11.3 MB (11301554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c54a7a0d1190cf72ddfa68662ea3a2304a24dee22be784222db411737343966`  
		Last Modified: Thu, 02 Dec 2021 03:53:05 GMT  
		Size: 4.3 MB (4342399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f386c5fc42a706d579b545a76f5bbdc7f4e6fcb70fd0a20b43dfc8a0af81fd`  
		Last Modified: Fri, 03 Dec 2021 04:13:07 GMT  
		Size: 13.4 MB (13386540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743dbe82dad4e858075662b8c7efc998c08b678a206a2453855bc23b998e16de`  
		Last Modified: Fri, 03 Dec 2021 04:13:05 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e66467af94904944cb25e19ddf0e736ba153c62237db494083f48db588de3`  
		Last Modified: Fri, 03 Dec 2021 04:13:30 GMT  
		Size: 58.4 MB (58402566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adee15ae00f32b97ce3556ce86a9785054717f722c4afb4fa7c957812dd7c20f`  
		Last Modified: Fri, 03 Dec 2021 04:13:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ae8b635e39b36ec87f48c309dd824ebba90bd8f60a1185ec2f8804e76b616f`  
		Last Modified: Fri, 03 Dec 2021 04:13:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:e72a3e1a4f061e6f7e63e73065f3d2b16ee6942928b0b04c9986ddc0f7846643
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124552730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a39f7ffbea20ad101dfeab0f56c0d67172e4166e9b4d76403eeefcbd86aef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:33 GMT
ADD file:3225671be4edc3599e29ebd06516b95573246e68bf29649c402ed87c03c109b5 in / 
# Wed, 17 Nov 2021 02:42:34 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:32:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:32:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 21:51:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 17 Nov 2021 21:51:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 17 Nov 2021 21:51:48 GMT
ENV KAPACITOR_VERSION=1.6.2
# Wed, 17 Nov 2021 21:51:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 17 Nov 2021 21:51:54 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 17 Nov 2021 21:51:54 GMT
EXPOSE 9092
# Wed, 17 Nov 2021 21:51:55 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 17 Nov 2021 21:51:57 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 17 Nov 2021 21:51:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 21:51:58 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c64a4bafe4ad6fc05fcc6d76d2a06f168f331ffbc87e518fb4ca4ea22e75527e`  
		Last Modified: Wed, 17 Nov 2021 02:51:11 GMT  
		Size: 43.2 MB (43174478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaddc7c2a37cd151a9001bbe7816f06f5f36ac6d53cc0d02fe2b327f85a2c7e`  
		Last Modified: Wed, 17 Nov 2021 13:40:24 GMT  
		Size: 10.2 MB (10216788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61401ffc70123532d1f4886b9ebd00e11d1155a2363117bf5aab10353c373dc9`  
		Last Modified: Wed, 17 Nov 2021 13:40:23 GMT  
		Size: 3.9 MB (3873891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb074bf5a62afe7dc5be79eea3c3d20629d53225b97bd84b3524d62e3dccaec`  
		Last Modified: Wed, 17 Nov 2021 21:52:18 GMT  
		Size: 12.8 MB (12846766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7b3488d8149e50e3ee19a0d88a8a2fda066b65ab5139fc907f9fd4b4ac8735`  
		Last Modified: Wed, 17 Nov 2021 21:52:17 GMT  
		Size: 2.8 KB (2823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159654be800b81cc902f6858f28a52623dcbba93b84ad53cfa78c1e09edd70`  
		Last Modified: Wed, 17 Nov 2021 21:52:40 GMT  
		Size: 54.4 MB (54437526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e501cab1d3a8ff59e6cdea40627c7cd507f8be0083ca732099f6555f3b1f4509`  
		Last Modified: Wed, 17 Nov 2021 21:52:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a001bc754967bc1a696da1d4f70fefc0f46337ebf837c18b94e128f8e9e16abe`  
		Last Modified: Wed, 17 Nov 2021 21:52:32 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
