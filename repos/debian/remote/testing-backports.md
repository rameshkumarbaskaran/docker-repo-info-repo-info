## `debian:testing-backports`

```console
$ docker pull debian@sha256:691642f7077ee55e51b98391a83e3856eaaff915c7577fed547c29ca46a72183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:e2d95eefc065e447643215c822ce8b28aa24cdb8d17059e92bb7e2653779b42c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacb81b5e85d92a71703bbc198614d75d12919e1b20b0649fc8016102b0d6699`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:11:42 GMT
ADD file:74681cecd762b2ba7998f4db71254724112eeeb0a1801289e92e9be9986fab3e in / 
# Wed, 01 Mar 2023 04:11:43 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:11:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bbf0dc8a79b520e97bfc1897d4020969033cda033c141208013b60015a6334e5`  
		Last Modified: Wed, 01 Mar 2023 04:16:58 GMT  
		Size: 49.2 MB (49237268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db4cabe2406c2ca2cc870fdbb1ba017edbd1b4c7d2e4e980e19c94fbe6b78fd`  
		Last Modified: Wed, 01 Mar 2023 04:17:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e8292f26ce78a896ae0c64fa23eefb753aa26c8a8b463aecbdcdaf01eba1734f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48073055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2334c7148c1590a9b2ede897e9ebb66510fa827a27bb86dac9d7abd4de8bc712`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:49:34 GMT
ADD file:2754fb0733bf053663be45fdf8749e4c88158b9b85a85403f9898c3dfb53215e in / 
# Wed, 01 Mar 2023 01:49:34 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:49:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3ec0704dfd86e01503ca7c8e58baaa3616684e2a382e2ae7ce46e3466830b2a1`  
		Last Modified: Wed, 01 Mar 2023 01:54:34 GMT  
		Size: 48.1 MB (48072831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2df0b944c64529f9142b7c44697dbabf1ad89eb38cbf101f8e7cf9c9f631e4d`  
		Last Modified: Wed, 01 Mar 2023 01:54:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a5c72bc480858008dce9e53be8987f2d867128717b34ca294b588dfcaeb96cca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45843511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef051962bd26553fbb717394fa6cbdd2fc88fce82d45c6290a15dd0a6c4911e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:59:11 GMT
ADD file:6820e6909f34bd7d88f849318c289d08246870bf48e194c42cbb0d2bfe92716d in / 
# Wed, 01 Mar 2023 01:59:11 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:59:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:26dc867e29a6399aa4a7d729a815dfe65dea3873cc63f402795055187cb4b88e`  
		Last Modified: Wed, 01 Mar 2023 02:06:03 GMT  
		Size: 45.8 MB (45843289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068607b3ca26ba811ce31d196a7341ea0ea63e14b171b5bcf9d2e0073fa18fbd`  
		Last Modified: Wed, 01 Mar 2023 02:06:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8d5a65033705d8a2fb721b5b88edf341ac749041722fab94e24268f6d8d1b7d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49328478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed79da747c3ac833850fb71dcccef818fc3cae48fe0f0072d1686c4253a4918`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:46:10 GMT
ADD file:659cb8b541c9a906fe60747ea4b6ec72bb4e3525e53ed5e749127f0d9cb21a15 in / 
# Thu, 23 Mar 2023 00:46:11 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:46:13 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e8c9f32eb3a01effeef152afae1272c7a3054f6070bca27f29886acb89e6b19b`  
		Last Modified: Thu, 23 Mar 2023 00:50:32 GMT  
		Size: 49.3 MB (49328258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba1173fc1cb5f8cfda391f83c4bee2665cc690c0c8faca06011a6816a3181e1`  
		Last Modified: Thu, 23 Mar 2023 00:50:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:5fdb01aae3b62fe4d7a01686d14001048040f08774150f6268120a90112c6695
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50324151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b73e7975be4d15e78c83ef6b297922431229afb9d796c497951a4a7cb7672d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:40:52 GMT
ADD file:f75b62250bff5d8572fec727da09f8822bc35c8a17646f1565d5ff0a13560c8b in / 
# Thu, 23 Mar 2023 00:40:53 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:40:56 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:852656c6bb930aeecbbfdb1c3b074519bbb3b8bb52bb3fad65e3ce1f2019c591`  
		Last Modified: Thu, 23 Mar 2023 00:46:03 GMT  
		Size: 50.3 MB (50323929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5032906680a8f70b9cce144641de62fd9b0024622de4d51ee63a80d0236bbfb`  
		Last Modified: Thu, 23 Mar 2023 00:46:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:10b6f73020588e97b4d6c35f65cbf479b1ab5110265e79e34fa80c2cb4f0416e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49245732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16940537906a118a74e5b233a78dbf1ccfb92383fafe7e6d9b7ba52d9d64f8aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:13:45 GMT
ADD file:1bf792d3c4330d4faf867dfb2e9689482bcfd0a8d9c641abd7cca9b6a218978f in / 
# Wed, 01 Mar 2023 02:13:50 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:14:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9abd347c7d1810d25b14d496d1aea23dffa3a1bdfd637405ff33a4f90244ddcc`  
		Last Modified: Wed, 01 Mar 2023 02:21:51 GMT  
		Size: 49.2 MB (49245506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1df3a413749712800dd37603aeba16f017976baed61398f73e1f2a83ce6ef8`  
		Last Modified: Wed, 01 Mar 2023 02:22:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:28adf9ba6e33bb79f122c1f341ef5babde4ba9ebc2a02303c5e2a29f2900cc32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53250400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea5f9e31ac248e0d284cf8a766cd348a80c299d37e9e94913c2057f1a4fabeb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:49:21 GMT
ADD file:802564bd8f691b73ccc068cc3c339c6a4c178bcf8383008e4f87a3774cb308b9 in / 
# Wed, 01 Mar 2023 04:49:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:49:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:adcb4bfc20e2eddc047aac97edc102514767c0f2b64f4f281f2e71651d1a97a9`  
		Last Modified: Wed, 01 Mar 2023 04:56:03 GMT  
		Size: 53.3 MB (53250177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b217a02928c343fd3b76cbda54988888d584c4cfc9e16ca62c30236316d6509`  
		Last Modified: Wed, 01 Mar 2023 04:56:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:eadb59faa50d6eedceffc18abe7b1164cbc64ecb2135c7132dfd7831983f7b0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47671241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c295ceb6b8759dabb96eddc9f82d81bf136acee54f2f9a002514aa9e639f1e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:12 GMT
ADD file:a96b8cacbcadb2068e0368c020589f4d2eae9fabb0965b387d5d9fc94831a1a5 in / 
# Thu, 23 Mar 2023 00:45:16 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:45:21 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:57560ce693355ef04b6283597b61cd71f7e8b7d7357b218eab0c8979bce7812e`  
		Last Modified: Thu, 23 Mar 2023 00:48:17 GMT  
		Size: 47.7 MB (47671021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe413e0a94d09e12d9238564e655958bc2e2ce663985bd7c11d778fadc2fdb76`  
		Last Modified: Thu, 23 Mar 2023 00:48:22 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
