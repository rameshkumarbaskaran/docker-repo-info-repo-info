## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:a489c3b1f646c4e9a4443714679d4528e6a297b053267db11759953834256368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:983a53bfb5cec227c03a60190ba42f7ef457c43269aa4bf80c958e907ea9b277
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70401916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f6454ea25793a0deb0c6dfbc7d16cc92b142239710aecb167c7c2d045c4e4f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:20:54 GMT
ADD file:375c01cd4aba0ddf77202decfeed5df5e3119ce460fcbf1f3b47f540a70b3864 in / 
# Thu, 10 Sep 2020 00:20:55 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:57:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:08d7334100fee80149028a0d0df44589b68e0c31592157808d18b68e6a572fd3`  
		Last Modified: Thu, 10 Sep 2020 00:33:04 GMT  
		Size: 51.9 MB (51906528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e2cbaa6fb6571d6e6f88e645061abb7c64ad18e76e900e6cfd8b80c5b36e84`  
		Last Modified: Thu, 10 Sep 2020 01:14:04 GMT  
		Size: 7.9 MB (7866624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70f330112cba767d415d7e4179b0dd52578b7685d2984ac61d9c3ba0884843a`  
		Last Modified: Thu, 10 Sep 2020 01:14:05 GMT  
		Size: 10.6 MB (10628764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ed9ccbfff779a62f91961710d791145443df6e6bc429bca5f8b6de0469d8c041
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67627368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa37aa1a3ad9ba7e9cb6257ca2d7a6092ae95d9903941402c40fd0039154c4d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:52:26 GMT
ADD file:f71e0d87d6d096130aa8dce14ce4db75b3a50725e9ba2aaab46f722a444291c9 in / 
# Wed, 09 Sep 2020 23:52:28 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:26:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:27:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:23e3aed2d466532e16ed7a54a2dc8d1ab497d8cd849573a7aa149e39f499eb77`  
		Last Modified: Thu, 10 Sep 2020 00:01:42 GMT  
		Size: 49.9 MB (49868299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57296d1a05acc9b2b6a146828bc5cd73f18a33087981038e29d2911236360b77`  
		Last Modified: Thu, 10 Sep 2020 00:51:46 GMT  
		Size: 7.4 MB (7444028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf329ff0c0ac4aa69298e3dae2a5539c0c7f11957ec83f3ae34b781fe1af258`  
		Last Modified: Thu, 10 Sep 2020 00:51:47 GMT  
		Size: 10.3 MB (10315041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eb9840f0d24827026c3cbab7359f646cccb1ef8c0e00687bece3fdcd08a7a6e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64766236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9b4affc873404a3218f70b686f4f83026a71e2984280843c0f2ddfb0353975`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:06:19 GMT
ADD file:1cf6aad11149d2248c2d64e694eea8993365bc92e69acb766de8eed5ff5ea516 in / 
# Thu, 10 Sep 2020 00:06:24 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:34:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:34:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d74d0dbf37b1422ef3ad4850d0d2337a00c1b3b940052b8328d43b006d7cac98`  
		Last Modified: Thu, 10 Sep 2020 00:16:52 GMT  
		Size: 47.6 MB (47622633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39be7872e432bb84dd6799e4f7aea36b8e63f90690ab9a44e04241ca2c86b8cd`  
		Last Modified: Thu, 10 Sep 2020 02:00:02 GMT  
		Size: 7.2 MB (7184503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba87750aacaf06d58ec51afa56e4906f26eb6e094675669d666733b31b9313be`  
		Last Modified: Thu, 10 Sep 2020 02:00:03 GMT  
		Size: 10.0 MB (9959100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:35a5885329a6dbbb07c536a70010845ea21cc1b981b64dcfb67adcbc8623afe9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69204517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987a312453e6e6a41af020dae3c276409466979d39b116d218e63e5704a0980d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:49:11 GMT
ADD file:82c33a26fb9be3ddaf17956539af2b205bdb6e28fe5ff1c7304ae8f294fe9581 in / 
# Wed, 09 Sep 2020 23:49:14 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:24:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5a65667356fa05b061c6733c879afab36ec44c6877341c2527e321b7206a26b2`  
		Last Modified: Wed, 09 Sep 2020 23:58:05 GMT  
		Size: 50.8 MB (50825395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730279b4ebb859065c90bbf90b3ac77059bd7d1e6cdc143106e0994dca9f4c59`  
		Last Modified: Thu, 10 Sep 2020 00:40:35 GMT  
		Size: 7.7 MB (7743447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a2c8b657c8d1b22dc8f6d15821f7035a315a0900f84b26ef36c86803feb02c`  
		Last Modified: Thu, 10 Sep 2020 00:40:35 GMT  
		Size: 10.6 MB (10635675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bc89058c28184be54723df2ebd02897bad4de1466fe302b1c919ec757e89e178
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72023148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1901f65826e101b143439b07a7e86e342f13c1186114603ef3194f88cb80cae1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:39:17 GMT
ADD file:f37f3bb35b6cca1cef993e4f39f48aab88ed76e0c47d97d61b4329fd8c5c5d03 in / 
# Wed, 09 Sep 2020 23:39:17 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 01:47:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4e5adf65093f5c6d699308a44f2173fac564be9f4e4daf24d82204c617b438d5`  
		Last Modified: Wed, 09 Sep 2020 23:45:45 GMT  
		Size: 53.0 MB (52969189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6830211bac3c1325ba53a3a4581992aa1d1916adf979c416833a3e9c0e9f24`  
		Last Modified: Thu, 10 Sep 2020 02:10:09 GMT  
		Size: 8.0 MB (8040370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7dd281614cde829dde09a35d83f8a4fa325cab69fafac8dba60a7b8950cae3`  
		Last Modified: Thu, 10 Sep 2020 02:10:09 GMT  
		Size: 11.0 MB (11013589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7f7605f9ca2196625517871a1ba2d0dc6f3731a0512c3a3c5d88caa761828051
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68600344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7792a320a2fc82afeca15f8d402bf74a3d0798c1e1dacc45d652f72015973dfd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:41:13 GMT
ADD file:9e3d31545fae8b44e8aa3ad24629d2336276c01e23dfbdde9885d01e61a54298 in / 
# Tue, 04 Aug 2020 06:41:14 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 10:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:34:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:249c58d6beef4ec2d380f0e2adf7ea99a80c295cddcf6f6bc3d6b463dfe44a05`  
		Last Modified: Tue, 04 Aug 2020 06:46:35 GMT  
		Size: 50.6 MB (50550783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049f809de28cc8d8e169ab9ee5721613f58fafdc670bbe6d66a1058fe998ee06`  
		Last Modified: Tue, 04 Aug 2020 10:47:30 GMT  
		Size: 7.5 MB (7450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d557e2093dc94091a8f931745b728c83f35ad977f14de65f1ec5db00bedf8580`  
		Last Modified: Tue, 04 Aug 2020 10:47:30 GMT  
		Size: 10.6 MB (10599039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:aeaa42a1b63cde153f7dbb627aa4c52c81f56c21645e4d193eda285dbdeab200
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75460376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8942149d5c0ad5935eab20334425efbb18175ae745257fea9a110358b4bed7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:54:23 GMT
ADD file:4529de4df0d9d1d1c2fc4ea683021e7ff678a24ca45c21d9dfaeb7c4dc1da51f in / 
# Thu, 10 Sep 2020 00:54:39 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:03:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 02:05:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6146fe38f8409e50a43aec229f36623c0f8c195d2cdf9bad02573a9d952a31a1`  
		Last Modified: Thu, 10 Sep 2020 01:23:23 GMT  
		Size: 55.8 MB (55774504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be50b08123b1849db4a42098bf6c8ac1fa2b4b66f3529542c22e6ebd32daaf8`  
		Last Modified: Thu, 10 Sep 2020 04:03:25 GMT  
		Size: 8.3 MB (8295948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc42e2c525916d192694c8773ed6f0bf7a72f3fa13d751e4087189acf6827c6`  
		Last Modified: Thu, 10 Sep 2020 04:03:24 GMT  
		Size: 11.4 MB (11389924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ee809f5a4ba794419fb939755e2dfb26f2ce6c345fde3cab40cad69f4f2f0e26
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68511194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8de6252a44f4d8218e1512a21cfb7b7a6fc7c263a743bb9c1e071dfdd1de03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:41:38 GMT
ADD file:d30705fcc57734260b517d32c4d610f1fe18e7d5faa78a22754774f5bf15eb9a in / 
# Wed, 09 Sep 2020 23:41:41 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:03:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:04:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b7fac0c9089d6ff39f6a7de3af657a8d580a7b074b45118b115539fd90213654`  
		Last Modified: Wed, 09 Sep 2020 23:45:45 GMT  
		Size: 50.5 MB (50468550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e4abf36c400373c14e1dc03dc7d41c9bb01249ef118a39b67294471b0cea9d`  
		Last Modified: Thu, 10 Sep 2020 00:11:24 GMT  
		Size: 7.5 MB (7537717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c291ff634945f7dc165f540d95c5d3958483aba31d45fbae0ee30d37ef13ca7`  
		Last Modified: Thu, 10 Sep 2020 00:11:25 GMT  
		Size: 10.5 MB (10504927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
