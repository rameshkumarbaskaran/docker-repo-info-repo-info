## `registry:latest`

```console
$ docker pull registry@sha256:bedef0f1d248508fe0a16d2cacea1d2e68e899b2220e2258f1b604e1f327d475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:affdb68e24c93262ee98a5bdc371e8f631568e9b4401375e7a0ecc705ac526b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9177133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773dbf02e42e2691c752b74e9b7745623c4279e4eeefe734804a32695e46e2f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 00:19:44 GMT
RUN apk add --no-cache ca-certificates
# Thu, 26 May 2022 21:30:55 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 26 May 2022 21:30:55 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 26 May 2022 21:30:55 GMT
VOLUME [/var/lib/registry]
# Thu, 26 May 2022 21:30:55 GMT
EXPOSE 5000
# Thu, 26 May 2022 21:30:55 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 26 May 2022 21:30:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 May 2022 21:30:55 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea60b727a1ce729d031ec1e4f2521a246e71bdb72d3fd9c9c04711cce80e1722`  
		Last Modified: Wed, 25 May 2022 00:24:05 GMT  
		Size: 271.8 KB (271822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87369050336f0361a8293961bc91964bfec56117b1d12c3b1cc7b8a6450f88b`  
		Last Modified: Thu, 26 May 2022 21:31:08 GMT  
		Size: 6.1 MB (6105809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69d20d3dd20002b58c1769fa21e355860b3d977b758de5aae93af9692179521`  
		Last Modified: Thu, 26 May 2022 21:31:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc30d7061437e87abdd8b0ae689d384ea38481eb040af340e7f7feb20537a88b`  
		Last Modified: Thu, 26 May 2022 21:31:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:72b37ab8c754099c1010f58420f29dfaa6207ea0c9449e4c9eadb591557628d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8549479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36e8f2d051b88e03f53f4e6833f8bf78528a2b33d32168539018c47dcbf2dec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 23 May 2022 19:49:32 GMT
ADD file:f7cee617575b5e5a7672d298a519bb8d8b5098efb90aa2a5d7b0510003457d52 in / 
# Mon, 23 May 2022 19:49:33 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 00:49:39 GMT
RUN apk add --no-cache ca-certificates
# Thu, 26 May 2022 21:51:13 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 26 May 2022 21:51:14 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 26 May 2022 21:51:14 GMT
VOLUME [/var/lib/registry]
# Thu, 26 May 2022 21:51:15 GMT
EXPOSE 5000
# Thu, 26 May 2022 21:51:15 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 26 May 2022 21:51:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 May 2022 21:51:16 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:79a25ccaf940855872635c06e7614d9b27dd38ffb5a8adfdb9274dfdc0ea0d87`  
		Last Modified: Mon, 23 May 2022 19:08:47 GMT  
		Size: 2.6 MB (2606142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c67ddc305b7f97a531083e369316343b3d19da2352e4e3274db751bba38e2`  
		Last Modified: Wed, 25 May 2022 00:59:27 GMT  
		Size: 272.0 KB (272047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f99e46990f1d706b6e001cc32feb20ef48b883cec96ef4d8a95584910bcb7`  
		Last Modified: Thu, 26 May 2022 21:51:52 GMT  
		Size: 5.7 MB (5670676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f8f03fc262a641510aabf9aad7d87f94c65106b80a51c547feb42cd400003c`  
		Last Modified: Thu, 26 May 2022 21:51:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc2aa1d6fd0010bd768116c8345f641ece7897d4144e79dc072d015137873cc`  
		Last Modified: Thu, 26 May 2022 21:51:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:9eb949d02f3b51cbc362e0e42b4febf2d8612e77170e7c651519c6cfe67c8ebd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8348898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26680098a66d9d4433fd4b29758f089095340d53a748d0438170cf8ccd1b043`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 23 May 2022 18:57:46 GMT
ADD file:72698cc08524b911ebaacf992490707e5a951ddd2fe6edb3fb598e9dc7155049 in / 
# Mon, 23 May 2022 18:57:47 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 03:51:19 GMT
RUN apk add --no-cache ca-certificates
# Thu, 26 May 2022 22:21:50 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 26 May 2022 22:21:51 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 26 May 2022 22:21:51 GMT
VOLUME [/var/lib/registry]
# Thu, 26 May 2022 22:21:51 GMT
EXPOSE 5000
# Thu, 26 May 2022 22:21:52 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 26 May 2022 22:21:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 May 2022 22:21:53 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:6366ba92f08e2418e90171f1e34bd86ecd50fdc95953b3f33b8943c143518eca`  
		Last Modified: Mon, 23 May 2022 18:59:17 GMT  
		Size: 2.4 MB (2411648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e4e5a89e8a0366f9710ba7cb04de284f11234b8cb3dba3e69e35a76dd1c62`  
		Last Modified: Wed, 25 May 2022 04:03:05 GMT  
		Size: 271.0 KB (270972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7872c8198c759824bf865020664dc2f3cccd0473887b2de7f670b9ea35e414bf`  
		Last Modified: Thu, 26 May 2022 22:22:29 GMT  
		Size: 5.7 MB (5665666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d0a2fd86e08a07292d2f1bc28c1b26c7ea789d0b0b4d104aa5843fc9fa6ff2`  
		Last Modified: Thu, 26 May 2022 22:22:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954be8af3f7eadbdafe21ea32edc12f4e5b0078cae3cca757a4632398f6876e`  
		Last Modified: Thu, 26 May 2022 22:22:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:e4ba779f37776b981d56050ec48463d9b903717a01e293e379de0779226c87dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8511216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a846de09651c90eaf2a2d0f9458c9cbb2065ae86ffe3aeabefa38c58a7e772`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 00:40:10 GMT
RUN apk add --no-cache ca-certificates
# Thu, 26 May 2022 21:52:46 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 26 May 2022 21:52:47 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 26 May 2022 21:52:47 GMT
VOLUME [/var/lib/registry]
# Thu, 26 May 2022 21:52:48 GMT
EXPOSE 5000
# Thu, 26 May 2022 21:52:50 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 26 May 2022 21:52:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 May 2022 21:52:51 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a3192eca97ce26527d2bdbb26d1130abcc1c9dd7b800ce2fd14619fa422640`  
		Last Modified: Wed, 25 May 2022 00:45:29 GMT  
		Size: 271.7 KB (271711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78a32497cf35ee91ada899c3c9b4db84a324f55511d3ac0796d6bf640b158b4`  
		Last Modified: Thu, 26 May 2022 21:53:11 GMT  
		Size: 5.5 MB (5544458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980c1fd5760c8c88fd16f70cea78b181bfef0659d34b06acd6664a6bfcef6e47`  
		Last Modified: Thu, 26 May 2022 21:53:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5c94d5e05dc31dc2341f96a1ec4aa4cb252eed9719bc808d18632281790033`  
		Last Modified: Thu, 26 May 2022 21:53:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:65c58d886bec80f756a35fafda7db3125d15c637f668d47241c52d4f121c0bac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8379833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb72baeec00ca7a92e86d101e0fd7897e0ecc41585ac4601856bb237b703395f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 23 May 2022 19:16:51 GMT
ADD file:6a5450c8a7cee3ceda59e7cb350c54df4139b0f7b7cf49c8b31bb9c01646c3cd in / 
# Mon, 23 May 2022 19:16:53 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 00:17:40 GMT
RUN apk add --no-cache ca-certificates
# Thu, 26 May 2022 21:30:29 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 26 May 2022 21:30:31 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 26 May 2022 21:30:35 GMT
VOLUME [/var/lib/registry]
# Thu, 26 May 2022 21:30:38 GMT
EXPOSE 5000
# Thu, 26 May 2022 21:30:41 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 26 May 2022 21:30:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 May 2022 21:30:47 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:d3deabf2a506ef6f5fa7c2a68bf27047574cef9908b30a97ff2d01ae539b089a`  
		Last Modified: Mon, 23 May 2022 19:09:13 GMT  
		Size: 2.8 MB (2789745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211c1f83aeafafff903bb460e7e24594fe138ebceeb1b56e898cf0158ea3daaf`  
		Last Modified: Wed, 25 May 2022 00:27:59 GMT  
		Size: 274.2 KB (274180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1926b73161fa2aede0ca1a5c8f92af3be254e02f7ba196e2516fdc56ca52a0`  
		Last Modified: Thu, 26 May 2022 21:31:10 GMT  
		Size: 5.3 MB (5315295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fc1cc84308b80491c18a2ed88c621451fedeac5dc6b9eacefd9cb70a5ccfd`  
		Last Modified: Thu, 26 May 2022 21:31:09 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05720f6f9b55b022c9479dd7740a7b7ece91061448bbbf16f74b2328165519dd`  
		Last Modified: Thu, 26 May 2022 21:31:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:1964b50a22d154ba9df4f69368ae13498bb2af4c891a2450c2fcd5c4577f1970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8664813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb089b3742ad08d96c3c51fd1a3a314350e9f6adb5c9e073632a81e20f243ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 23 May 2022 19:41:59 GMT
ADD file:e1852d8ef555a0d3ef6d0b74a898720c82bb9f491430b06a0dd0499497ce118e in / 
# Mon, 23 May 2022 19:42:10 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 00:41:57 GMT
RUN apk add --no-cache ca-certificates
# Thu, 26 May 2022 21:54:08 GMT
RUN set -eux; 	version='2.8.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='f1a376964912a5fd7d588107ebe5185da77803244e15476d483c945959347ee2' ;; 		aarch64) arch='arm64';   sha256='4c588c8e62c9a84f1eecfba4c842fe363b91be87fd42e3b5dac45148a2f46c52' ;; 		armhf)   arch='armv6';   sha256='d711b3b6e77f3acc7c89fad9310413ef145751ac702627dc1fa89991bf3b6104' ;; 		armv7)   arch='armv7';   sha256='d2f2180c1a847056f9c5dcfd1d6fda4c6086d126204541e0ed047c04f30a0f91' ;; 		ppc64le) arch='ppc64le'; sha256='ca77cdfb7b1415869558c118b5e783bb9d695a74d8426a0bd8d8a39beb23fb85' ;; 		s390x)   arch='s390x';   sha256='3e505af15c562870869441d5d1f79988c3c666b9a4370894ecf2f064860b48ba' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Thu, 26 May 2022 21:54:09 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 26 May 2022 21:54:09 GMT
VOLUME [/var/lib/registry]
# Thu, 26 May 2022 21:54:09 GMT
EXPOSE 5000
# Thu, 26 May 2022 21:54:10 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 26 May 2022 21:54:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 May 2022 21:54:11 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:af1ac1a73384e058591d04d19bc05a06781cc32d52d4593b468d6cb95eda9858`  
		Last Modified: Mon, 23 May 2022 19:43:36 GMT  
		Size: 2.6 MB (2580494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e497ff1a375465e6a6ba78259a6f2e9f7986cf27789ba79ddfd1cca023a160`  
		Last Modified: Wed, 25 May 2022 00:50:39 GMT  
		Size: 272.2 KB (272155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9494e4392aea246bd0d0648081f17e0624142428b4f7b7fabdd63520180b9ea8`  
		Last Modified: Thu, 26 May 2022 21:54:33 GMT  
		Size: 5.8 MB (5811551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6390623280bb21334edbd58b2668cefec5dc73d0c2f51198c301e8b26156e709`  
		Last Modified: Thu, 26 May 2022 21:54:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65475fe64c2f540793d04033940afe36af7bfa864a4c2186127186851359cbec`  
		Last Modified: Thu, 26 May 2022 21:54:32 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
