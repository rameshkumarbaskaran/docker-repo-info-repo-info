<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20210525.0`](#amazonlinux20202105250)
-	[`amazonlinux:2.0.20210525.0-with-sources`](#amazonlinux20202105250-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20210521.1`](#amazonlinux2018030202105211)
-	[`amazonlinux:2018.03.0.20210521.1-with-sources`](#amazonlinux2018030202105211-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:d8db8960d84895fb10e491080d4069ac542aa06205a9ccf3af202a927d561bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7326b7afba891588bce0cb6a6244f9bb205bbbb7ad7b6a719e356ad8e878102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62233767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07431b5cc2148664c7fd5c2f4e6c47bc7386eca1abd67ccc506240521e2a6dc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:bd7aca583738a44ccabf6582caa32ea1b3dbd5ffff26e0606c0f1a6a0515d8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:80878ae39f9fe1a9a950ff72ea175f41144032442c3e84f3635a135f7de32f57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449096717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce78d0c69b908a315c3a8930d9e6bccef3317b485528e31c72acff0cb546755a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 23:47:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-dc5d92c927a9f79aab7658e5c05df877dd40282d7bf9b4b11a5eb11b225cb7ad.tar.gz"  && echo "03509f1ca8f0593cf761a9fda3dc71baf0f45752a0d8908a04ccd9937bd1ddfc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b4f3ad9bb7c123e4d3b3582e82bff05e5f83438191ad98a2d271e235ff1c2`  
		Last Modified: Thu, 03 Jun 2021 23:48:58 GMT  
		Size: 386.9 MB (386862950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:c256d49ba173a51ef99c8574f5bc57d9b65a6467fab55dbbc70629a0744644bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f6a328fd2a8abac76b0672511f9577695565a62cb77d71b14984bba9016da0b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61949057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe81afbc7b998974ada34046c4920bb8a50bf3e13994af09f9560f83e8097e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:53270771209c5d5984ee2ac029b0c9d14469da1261d96b2b650c639ccd7039ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63448527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8638d00643c56ef0fd1337933a45b4fc52ab61891c40078088e7d2b2245fbc86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:6f9822eee42debc2158764c7051f185ba4ff0b71737223bb000e8bd043b77399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:510f0a1078b46a1b3d3794c6338e79822661dfaf64c071411d2cc942277b5121
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542832809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f34482269be861bd6e0bed4c3b2bb355765da4dbe5d83580a9374a2d2297cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:21:51 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ee793b7ad6731c03046e8e2d97f0d9083f5ff5f0e6c8817ab64b17ffae75b9da.tar.gz"  && echo "428461ebff94149f216b4805145f5430c52e306238f4a5df82e0f81328891e6b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070c24b45b14bcccd32768a67b8cf640c2bd8c69cfc4ddbca681aa244d8d8fc6`  
		Last Modified: Mon, 14 Jun 2021 22:22:55 GMT  
		Size: 480.9 MB (480883752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6bc07f7fe40ad0736eeb784c65a0f7549ee3748bcc32ba99fd8f762c1809a038
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.3 MB (544332281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99f1d287c49fcadf915bddbd8e8eeb0d122d4ad7b79b6b20d442aa3077654c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:39:48 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ee793b7ad6731c03046e8e2d97f0d9083f5ff5f0e6c8817ab64b17ffae75b9da.tar.gz"  && echo "428461ebff94149f216b4805145f5430c52e306238f4a5df82e0f81328891e6b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d101914055c1e9156b29d4d91e0821e935297b07837a6ed9a726f1271499fd5a`  
		Last Modified: Mon, 14 Jun 2021 22:41:01 GMT  
		Size: 480.9 MB (480883754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20210525.0`

```console
$ docker pull amazonlinux@sha256:c256d49ba173a51ef99c8574f5bc57d9b65a6467fab55dbbc70629a0744644bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20210525.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f6a328fd2a8abac76b0672511f9577695565a62cb77d71b14984bba9016da0b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61949057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe81afbc7b998974ada34046c4920bb8a50bf3e13994af09f9560f83e8097e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20210525.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:53270771209c5d5984ee2ac029b0c9d14469da1261d96b2b650c639ccd7039ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63448527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8638d00643c56ef0fd1337933a45b4fc52ab61891c40078088e7d2b2245fbc86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20210525.0-with-sources`

```console
$ docker pull amazonlinux@sha256:6f9822eee42debc2158764c7051f185ba4ff0b71737223bb000e8bd043b77399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20210525.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:510f0a1078b46a1b3d3794c6338e79822661dfaf64c071411d2cc942277b5121
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542832809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f34482269be861bd6e0bed4c3b2bb355765da4dbe5d83580a9374a2d2297cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:21:51 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ee793b7ad6731c03046e8e2d97f0d9083f5ff5f0e6c8817ab64b17ffae75b9da.tar.gz"  && echo "428461ebff94149f216b4805145f5430c52e306238f4a5df82e0f81328891e6b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070c24b45b14bcccd32768a67b8cf640c2bd8c69cfc4ddbca681aa244d8d8fc6`  
		Last Modified: Mon, 14 Jun 2021 22:22:55 GMT  
		Size: 480.9 MB (480883752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20210525.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6bc07f7fe40ad0736eeb784c65a0f7549ee3748bcc32ba99fd8f762c1809a038
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.3 MB (544332281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99f1d287c49fcadf915bddbd8e8eeb0d122d4ad7b79b6b20d442aa3077654c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:39:48 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ee793b7ad6731c03046e8e2d97f0d9083f5ff5f0e6c8817ab64b17ffae75b9da.tar.gz"  && echo "428461ebff94149f216b4805145f5430c52e306238f4a5df82e0f81328891e6b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d101914055c1e9156b29d4d91e0821e935297b07837a6ed9a726f1271499fd5a`  
		Last Modified: Mon, 14 Jun 2021 22:41:01 GMT  
		Size: 480.9 MB (480883754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:d8db8960d84895fb10e491080d4069ac542aa06205a9ccf3af202a927d561bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7326b7afba891588bce0cb6a6244f9bb205bbbb7ad7b6a719e356ad8e878102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62233767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07431b5cc2148664c7fd5c2f4e6c47bc7386eca1abd67ccc506240521e2a6dc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:bd7aca583738a44ccabf6582caa32ea1b3dbd5ffff26e0606c0f1a6a0515d8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:80878ae39f9fe1a9a950ff72ea175f41144032442c3e84f3635a135f7de32f57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449096717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce78d0c69b908a315c3a8930d9e6bccef3317b485528e31c72acff0cb546755a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 23:47:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-dc5d92c927a9f79aab7658e5c05df877dd40282d7bf9b4b11a5eb11b225cb7ad.tar.gz"  && echo "03509f1ca8f0593cf761a9fda3dc71baf0f45752a0d8908a04ccd9937bd1ddfc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b4f3ad9bb7c123e4d3b3582e82bff05e5f83438191ad98a2d271e235ff1c2`  
		Last Modified: Thu, 03 Jun 2021 23:48:58 GMT  
		Size: 386.9 MB (386862950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20210521.1`

```console
$ docker pull amazonlinux@sha256:d8db8960d84895fb10e491080d4069ac542aa06205a9ccf3af202a927d561bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03.0.20210521.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7326b7afba891588bce0cb6a6244f9bb205bbbb7ad7b6a719e356ad8e878102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62233767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07431b5cc2148664c7fd5c2f4e6c47bc7386eca1abd67ccc506240521e2a6dc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20210521.1-with-sources`

```console
$ docker pull amazonlinux@sha256:bd7aca583738a44ccabf6582caa32ea1b3dbd5ffff26e0606c0f1a6a0515d8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03.0.20210521.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:80878ae39f9fe1a9a950ff72ea175f41144032442c3e84f3635a135f7de32f57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449096717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce78d0c69b908a315c3a8930d9e6bccef3317b485528e31c72acff0cb546755a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Jun 2021 23:47:34 GMT
ADD file:d54600120dd0df387f02c9986b95553c7be4690d3226e5693a0621e1bbba9c79 in / 
# Thu, 03 Jun 2021 23:47:35 GMT
CMD ["/bin/bash"]
# Thu, 03 Jun 2021 23:47:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-dc5d92c927a9f79aab7658e5c05df877dd40282d7bf9b4b11a5eb11b225cb7ad.tar.gz"  && echo "03509f1ca8f0593cf761a9fda3dc71baf0f45752a0d8908a04ccd9937bd1ddfc  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:8aa1c9f768e700368fba92ab67c462b5757d5e5d801b2309ce0ac018cc7a13e9`  
		Last Modified: Thu, 03 Jun 2021 23:48:24 GMT  
		Size: 62.2 MB (62233767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b4f3ad9bb7c123e4d3b3582e82bff05e5f83438191ad98a2d271e235ff1c2`  
		Last Modified: Thu, 03 Jun 2021 23:48:58 GMT  
		Size: 386.9 MB (386862950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:c256d49ba173a51ef99c8574f5bc57d9b65a6467fab55dbbc70629a0744644bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f6a328fd2a8abac76b0672511f9577695565a62cb77d71b14984bba9016da0b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61949057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe81afbc7b998974ada34046c4920bb8a50bf3e13994af09f9560f83e8097e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:53270771209c5d5984ee2ac029b0c9d14469da1261d96b2b650c639ccd7039ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63448527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8638d00643c56ef0fd1337933a45b4fc52ab61891c40078088e7d2b2245fbc86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:6f9822eee42debc2158764c7051f185ba4ff0b71737223bb000e8bd043b77399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:510f0a1078b46a1b3d3794c6338e79822661dfaf64c071411d2cc942277b5121
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542832809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f34482269be861bd6e0bed4c3b2bb355765da4dbe5d83580a9374a2d2297cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:21:51 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ee793b7ad6731c03046e8e2d97f0d9083f5ff5f0e6c8817ab64b17ffae75b9da.tar.gz"  && echo "428461ebff94149f216b4805145f5430c52e306238f4a5df82e0f81328891e6b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070c24b45b14bcccd32768a67b8cf640c2bd8c69cfc4ddbca681aa244d8d8fc6`  
		Last Modified: Mon, 14 Jun 2021 22:22:55 GMT  
		Size: 480.9 MB (480883752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6bc07f7fe40ad0736eeb784c65a0f7549ee3748bcc32ba99fd8f762c1809a038
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.3 MB (544332281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99f1d287c49fcadf915bddbd8e8eeb0d122d4ad7b79b6b20d442aa3077654c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:39:48 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-ee793b7ad6731c03046e8e2d97f0d9083f5ff5f0e6c8817ab64b17ffae75b9da.tar.gz"  && echo "428461ebff94149f216b4805145f5430c52e306238f4a5df82e0f81328891e6b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d101914055c1e9156b29d4d91e0821e935297b07837a6ed9a726f1271499fd5a`  
		Last Modified: Mon, 14 Jun 2021 22:41:01 GMT  
		Size: 480.9 MB (480883754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
