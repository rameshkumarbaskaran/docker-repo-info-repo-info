<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20220912.1`](#amazonlinux20202209121)
-	[`amazonlinux:2.0.20220912.1-with-sources`](#amazonlinux20202209121-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20220802.0`](#amazonlinux2018030202208020)
-	[`amazonlinux:2018.03.0.20220802.0-with-sources`](#amazonlinux2018030202208020-with-sources)
-	[`amazonlinux:2022`](#amazonlinux2022)
-	[`amazonlinux:2022-with-sources`](#amazonlinux2022-with-sources)
-	[`amazonlinux:2022.0.20220831.1`](#amazonlinux20220202208311)
-	[`amazonlinux:2022.0.20220831.1-with-sources`](#amazonlinux20220202208311-with-sources)
-	[`amazonlinux:devel`](#amazonlinuxdevel)
-	[`amazonlinux:devel-with-sources`](#amazonlinuxdevel-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:cc88d1da2efe66faa3b86ef71e70e8b7b52822f1bebdd1dd7b56c7f0e3cbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ba0ec71b51f66eeb3c2a808f463fa79dffa362de472e3e6c1650b0953471b227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80a9b43a329751b9a765fb6d1e788afb43419119cb4946c578832fb43fb8a84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:4cc664bb668e2e073fb39df0fee7e85317f34850ac7b117fb832a1a3c7b47e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e904f4b8c4ac1bd2ee165c00d8c0854558b9a799a31c0a265433f1ed453c2970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232eb238b33b7e870dd055314fe8ca6e936ad5f353e199a4f203ec82ca7fe5de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 18:20:10 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-77f3d99b447b0774a1bbba85498486869e097db4118c05994ac137d64f0f07bb.tar.gz"     && echo "c428ed82c12be347f1150a419dc16d997020583bda0f076e10a0f34b88df6363  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb07ac98d11436de390efdab7fd63c37b7afabc8b88176ca190a39ba9a6cb12`  
		Last Modified: Thu, 25 Aug 2022 18:21:18 GMT  
		Size: 452.7 MB (452687867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:b393108d01e77ff923d602f837fabb1aa545e8b913fbb1f7130d2ca30bde3c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c5e654f04302f2f88bdc5fe9644b7a096405205432a3738fc2ca6d4b766b6037
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62303269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bdb519be2070a170aee5940166344f2a871e7d22887366c0a30406094727bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:10c927b25ed56533d46fc4f2ac0085bc5f8839527c83ee5ea395753b019d899f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63912418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c44e7db5ae05cce1a4890c4507b657d00a595765e478417de6cbe69d4d4eb01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:a4a7095f6cae0281cf3a5f357eda5174a0e2ee3fb1f584858f2740c0958a7eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f1c531eaf600c693158c1d1ebbead9146809d78fab280d8bb9fa3b255b8c5af0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.4 MB (486378202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1900d5d0b057d3ad0be96c67ba2666b4016b5a9e87c34e4442e61d12d4002336`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:19:40 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d7c2b2aa50fe3ff7023a3909084d659b7f234ce37cb2b8a54bc449bb682a27`  
		Last Modified: Thu, 22 Sep 2022 19:20:48 GMT  
		Size: 424.1 MB (424074933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c64709a723326277e8bd139dee26c099248a5cfdc15af39276fdab5bfab370e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487987310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e561a7921606d2497a6dd0c931d14e2c4efc3c741a9a665cef47c145e63222`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:39:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366907dea1a523b535578b50385542ee460f0d786719b57a5b8a57f84d86c59c`  
		Last Modified: Thu, 22 Sep 2022 19:41:14 GMT  
		Size: 424.1 MB (424074892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220912.1`

```console
$ docker pull amazonlinux@sha256:b393108d01e77ff923d602f837fabb1aa545e8b913fbb1f7130d2ca30bde3c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220912.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c5e654f04302f2f88bdc5fe9644b7a096405205432a3738fc2ca6d4b766b6037
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62303269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bdb519be2070a170aee5940166344f2a871e7d22887366c0a30406094727bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20220912.1` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:10c927b25ed56533d46fc4f2ac0085bc5f8839527c83ee5ea395753b019d899f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63912418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c44e7db5ae05cce1a4890c4507b657d00a595765e478417de6cbe69d4d4eb01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220912.1-with-sources`

```console
$ docker pull amazonlinux@sha256:a4a7095f6cae0281cf3a5f357eda5174a0e2ee3fb1f584858f2740c0958a7eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220912.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f1c531eaf600c693158c1d1ebbead9146809d78fab280d8bb9fa3b255b8c5af0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.4 MB (486378202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1900d5d0b057d3ad0be96c67ba2666b4016b5a9e87c34e4442e61d12d4002336`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:19:40 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d7c2b2aa50fe3ff7023a3909084d659b7f234ce37cb2b8a54bc449bb682a27`  
		Last Modified: Thu, 22 Sep 2022 19:20:48 GMT  
		Size: 424.1 MB (424074933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20220912.1-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c64709a723326277e8bd139dee26c099248a5cfdc15af39276fdab5bfab370e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487987310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e561a7921606d2497a6dd0c931d14e2c4efc3c741a9a665cef47c145e63222`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:39:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366907dea1a523b535578b50385542ee460f0d786719b57a5b8a57f84d86c59c`  
		Last Modified: Thu, 22 Sep 2022 19:41:14 GMT  
		Size: 424.1 MB (424074892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:cc88d1da2efe66faa3b86ef71e70e8b7b52822f1bebdd1dd7b56c7f0e3cbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ba0ec71b51f66eeb3c2a808f463fa79dffa362de472e3e6c1650b0953471b227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80a9b43a329751b9a765fb6d1e788afb43419119cb4946c578832fb43fb8a84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:4cc664bb668e2e073fb39df0fee7e85317f34850ac7b117fb832a1a3c7b47e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e904f4b8c4ac1bd2ee165c00d8c0854558b9a799a31c0a265433f1ed453c2970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232eb238b33b7e870dd055314fe8ca6e936ad5f353e199a4f203ec82ca7fe5de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 18:20:10 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-77f3d99b447b0774a1bbba85498486869e097db4118c05994ac137d64f0f07bb.tar.gz"     && echo "c428ed82c12be347f1150a419dc16d997020583bda0f076e10a0f34b88df6363  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb07ac98d11436de390efdab7fd63c37b7afabc8b88176ca190a39ba9a6cb12`  
		Last Modified: Thu, 25 Aug 2022 18:21:18 GMT  
		Size: 452.7 MB (452687867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20220802.0`

```console
$ docker pull amazonlinux@sha256:cc88d1da2efe66faa3b86ef71e70e8b7b52822f1bebdd1dd7b56c7f0e3cbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20220802.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ba0ec71b51f66eeb3c2a808f463fa79dffa362de472e3e6c1650b0953471b227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80a9b43a329751b9a765fb6d1e788afb43419119cb4946c578832fb43fb8a84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20220802.0-with-sources`

```console
$ docker pull amazonlinux@sha256:4cc664bb668e2e073fb39df0fee7e85317f34850ac7b117fb832a1a3c7b47e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20220802.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:e904f4b8c4ac1bd2ee165c00d8c0854558b9a799a31c0a265433f1ed453c2970
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232eb238b33b7e870dd055314fe8ca6e936ad5f353e199a4f203ec82ca7fe5de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 18:19:48 GMT
ADD file:9e8cce1e42cea635edfdd37709f35ae6c2245a7083686c2943b7d13dea774f7d in / 
# Thu, 25 Aug 2022 18:19:49 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 18:20:10 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-77f3d99b447b0774a1bbba85498486869e097db4118c05994ac137d64f0f07bb.tar.gz"     && echo "c428ed82c12be347f1150a419dc16d997020583bda0f076e10a0f34b88df6363  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f08ecab7f1156b852159d72973eed2aacf858af0dbc76980151a20d8a80c0d30`  
		Last Modified: Thu, 25 Aug 2022 18:20:49 GMT  
		Size: 62.3 MB (62346886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb07ac98d11436de390efdab7fd63c37b7afabc8b88176ca190a39ba9a6cb12`  
		Last Modified: Thu, 25 Aug 2022 18:21:18 GMT  
		Size: 452.7 MB (452687867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022`

```console
$ docker pull amazonlinux@sha256:d26e31b5b4bb811a12cb868453a980a9ae53338020130521b67068cec9cabcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7301b45cf224105e4892bd17af6830ee84bd0d526a422dc6b3d383016fc3883b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57840745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af53369432b6a25196be571d33443209d8d94bdb440a378273eebc3262e3ba3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:19:43 GMT
ADD file:5019265631ee9bf27ce7360e76e53ca31276f85743f8f89ebbae0db6682520d9 in / 
# Wed, 07 Sep 2022 19:19:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c011f68cda3c0b264e794a7a2ed6621c014d944eab2c3c47bb1260e0279aae63`  
		Last Modified: Sat, 03 Sep 2022 04:05:43 GMT  
		Size: 57.8 MB (57840745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:5a12fea5a2f227cd2abb0dca3227e3aab5d8685b301a291334bfff984057ee86
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56647188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33ed3691d9394a4bc76c2dbb71ea8b2b65e6e0d1cef0ed5f537f5e89f501718`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:39:40 GMT
ADD file:14de8dca6a69b386ae8bed6870c1e376b67ce8e35574747f3faea9cf143bca6e in / 
# Wed, 07 Sep 2022 19:39:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00ee01a8a4f0d3d97470c0d349a8ee4b534ef5a20a1c1abec5e0697493d8c08d`  
		Last Modified: Wed, 07 Sep 2022 19:40:41 GMT  
		Size: 56.6 MB (56647188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022-with-sources`

```console
$ docker pull amazonlinux@sha256:c4e634a38404c34ac9f4b284bb68641df5c67ea6ff176f9022b06ceef2274a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:71644fe2ef5416f8ceabf402da7c4174fe750599076e106d9e9e6a4f89f52892
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392646533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ceb4a4a8fb4917a472d3255b0b9f526a6523ad4a66219e31d1aa9ad902bebc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:19:43 GMT
ADD file:5019265631ee9bf27ce7360e76e53ca31276f85743f8f89ebbae0db6682520d9 in / 
# Wed, 07 Sep 2022 19:19:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Sep 2022 19:20:03 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-398599ffb8d0f6fb08e1b8d66966668452019fb99181907d93c4c560edce242b.tar.gz"     && echo "9045a697728eafb7c14d20a4170b7906c2f813b55a5bb32635f1963318df140c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:c011f68cda3c0b264e794a7a2ed6621c014d944eab2c3c47bb1260e0279aae63`  
		Last Modified: Sat, 03 Sep 2022 04:05:43 GMT  
		Size: 57.8 MB (57840745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774b64e073109e8601db92af4778785b74981d0a66bb35ed640af8a8425ce28e`  
		Last Modified: Wed, 07 Sep 2022 19:21:07 GMT  
		Size: 334.8 MB (334805788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:53c32bc4a8fea84710fbfe1933b1b84db108eb76ee3c20b3b673e6bf9e331ba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.5 MB (391452945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e68a8cd162c06fc4c4bc68291eb191aadd029d78a8e0dec6b8652231c5775f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:39:40 GMT
ADD file:14de8dca6a69b386ae8bed6870c1e376b67ce8e35574747f3faea9cf143bca6e in / 
# Wed, 07 Sep 2022 19:39:41 GMT
CMD ["/bin/bash"]
# Wed, 07 Sep 2022 19:40:00 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-398599ffb8d0f6fb08e1b8d66966668452019fb99181907d93c4c560edce242b.tar.gz"     && echo "9045a697728eafb7c14d20a4170b7906c2f813b55a5bb32635f1963318df140c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:00ee01a8a4f0d3d97470c0d349a8ee4b534ef5a20a1c1abec5e0697493d8c08d`  
		Last Modified: Wed, 07 Sep 2022 19:40:41 GMT  
		Size: 56.6 MB (56647188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b245692459684d75b294e1d16f2407220fe53f4ae799e5a91d34fe73061cd`  
		Last Modified: Wed, 07 Sep 2022 19:41:38 GMT  
		Size: 334.8 MB (334805757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20220831.1`

```console
$ docker pull amazonlinux@sha256:d26e31b5b4bb811a12cb868453a980a9ae53338020130521b67068cec9cabcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022.0.20220831.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7301b45cf224105e4892bd17af6830ee84bd0d526a422dc6b3d383016fc3883b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57840745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af53369432b6a25196be571d33443209d8d94bdb440a378273eebc3262e3ba3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:19:43 GMT
ADD file:5019265631ee9bf27ce7360e76e53ca31276f85743f8f89ebbae0db6682520d9 in / 
# Wed, 07 Sep 2022 19:19:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c011f68cda3c0b264e794a7a2ed6621c014d944eab2c3c47bb1260e0279aae63`  
		Last Modified: Sat, 03 Sep 2022 04:05:43 GMT  
		Size: 57.8 MB (57840745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022.0.20220831.1` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:5a12fea5a2f227cd2abb0dca3227e3aab5d8685b301a291334bfff984057ee86
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56647188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33ed3691d9394a4bc76c2dbb71ea8b2b65e6e0d1cef0ed5f537f5e89f501718`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:39:40 GMT
ADD file:14de8dca6a69b386ae8bed6870c1e376b67ce8e35574747f3faea9cf143bca6e in / 
# Wed, 07 Sep 2022 19:39:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00ee01a8a4f0d3d97470c0d349a8ee4b534ef5a20a1c1abec5e0697493d8c08d`  
		Last Modified: Wed, 07 Sep 2022 19:40:41 GMT  
		Size: 56.6 MB (56647188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20220831.1-with-sources`

```console
$ docker pull amazonlinux@sha256:c4e634a38404c34ac9f4b284bb68641df5c67ea6ff176f9022b06ceef2274a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022.0.20220831.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:71644fe2ef5416f8ceabf402da7c4174fe750599076e106d9e9e6a4f89f52892
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392646533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ceb4a4a8fb4917a472d3255b0b9f526a6523ad4a66219e31d1aa9ad902bebc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:19:43 GMT
ADD file:5019265631ee9bf27ce7360e76e53ca31276f85743f8f89ebbae0db6682520d9 in / 
# Wed, 07 Sep 2022 19:19:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Sep 2022 19:20:03 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-398599ffb8d0f6fb08e1b8d66966668452019fb99181907d93c4c560edce242b.tar.gz"     && echo "9045a697728eafb7c14d20a4170b7906c2f813b55a5bb32635f1963318df140c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:c011f68cda3c0b264e794a7a2ed6621c014d944eab2c3c47bb1260e0279aae63`  
		Last Modified: Sat, 03 Sep 2022 04:05:43 GMT  
		Size: 57.8 MB (57840745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774b64e073109e8601db92af4778785b74981d0a66bb35ed640af8a8425ce28e`  
		Last Modified: Wed, 07 Sep 2022 19:21:07 GMT  
		Size: 334.8 MB (334805788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022.0.20220831.1-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:53c32bc4a8fea84710fbfe1933b1b84db108eb76ee3c20b3b673e6bf9e331ba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.5 MB (391452945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e68a8cd162c06fc4c4bc68291eb191aadd029d78a8e0dec6b8652231c5775f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:39:40 GMT
ADD file:14de8dca6a69b386ae8bed6870c1e376b67ce8e35574747f3faea9cf143bca6e in / 
# Wed, 07 Sep 2022 19:39:41 GMT
CMD ["/bin/bash"]
# Wed, 07 Sep 2022 19:40:00 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-398599ffb8d0f6fb08e1b8d66966668452019fb99181907d93c4c560edce242b.tar.gz"     && echo "9045a697728eafb7c14d20a4170b7906c2f813b55a5bb32635f1963318df140c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:00ee01a8a4f0d3d97470c0d349a8ee4b534ef5a20a1c1abec5e0697493d8c08d`  
		Last Modified: Wed, 07 Sep 2022 19:40:41 GMT  
		Size: 56.6 MB (56647188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b245692459684d75b294e1d16f2407220fe53f4ae799e5a91d34fe73061cd`  
		Last Modified: Wed, 07 Sep 2022 19:41:38 GMT  
		Size: 334.8 MB (334805757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel`

```console
$ docker pull amazonlinux@sha256:d26e31b5b4bb811a12cb868453a980a9ae53338020130521b67068cec9cabcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7301b45cf224105e4892bd17af6830ee84bd0d526a422dc6b3d383016fc3883b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57840745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af53369432b6a25196be571d33443209d8d94bdb440a378273eebc3262e3ba3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:19:43 GMT
ADD file:5019265631ee9bf27ce7360e76e53ca31276f85743f8f89ebbae0db6682520d9 in / 
# Wed, 07 Sep 2022 19:19:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c011f68cda3c0b264e794a7a2ed6621c014d944eab2c3c47bb1260e0279aae63`  
		Last Modified: Sat, 03 Sep 2022 04:05:43 GMT  
		Size: 57.8 MB (57840745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:5a12fea5a2f227cd2abb0dca3227e3aab5d8685b301a291334bfff984057ee86
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56647188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33ed3691d9394a4bc76c2dbb71ea8b2b65e6e0d1cef0ed5f537f5e89f501718`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:39:40 GMT
ADD file:14de8dca6a69b386ae8bed6870c1e376b67ce8e35574747f3faea9cf143bca6e in / 
# Wed, 07 Sep 2022 19:39:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00ee01a8a4f0d3d97470c0d349a8ee4b534ef5a20a1c1abec5e0697493d8c08d`  
		Last Modified: Wed, 07 Sep 2022 19:40:41 GMT  
		Size: 56.6 MB (56647188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:c4e634a38404c34ac9f4b284bb68641df5c67ea6ff176f9022b06ceef2274a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:71644fe2ef5416f8ceabf402da7c4174fe750599076e106d9e9e6a4f89f52892
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392646533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ceb4a4a8fb4917a472d3255b0b9f526a6523ad4a66219e31d1aa9ad902bebc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:19:43 GMT
ADD file:5019265631ee9bf27ce7360e76e53ca31276f85743f8f89ebbae0db6682520d9 in / 
# Wed, 07 Sep 2022 19:19:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Sep 2022 19:20:03 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-398599ffb8d0f6fb08e1b8d66966668452019fb99181907d93c4c560edce242b.tar.gz"     && echo "9045a697728eafb7c14d20a4170b7906c2f813b55a5bb32635f1963318df140c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:c011f68cda3c0b264e794a7a2ed6621c014d944eab2c3c47bb1260e0279aae63`  
		Last Modified: Sat, 03 Sep 2022 04:05:43 GMT  
		Size: 57.8 MB (57840745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774b64e073109e8601db92af4778785b74981d0a66bb35ed640af8a8425ce28e`  
		Last Modified: Wed, 07 Sep 2022 19:21:07 GMT  
		Size: 334.8 MB (334805788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:53c32bc4a8fea84710fbfe1933b1b84db108eb76ee3c20b3b673e6bf9e331ba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.5 MB (391452945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e68a8cd162c06fc4c4bc68291eb191aadd029d78a8e0dec6b8652231c5775f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Sep 2022 19:39:40 GMT
ADD file:14de8dca6a69b386ae8bed6870c1e376b67ce8e35574747f3faea9cf143bca6e in / 
# Wed, 07 Sep 2022 19:39:41 GMT
CMD ["/bin/bash"]
# Wed, 07 Sep 2022 19:40:00 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-398599ffb8d0f6fb08e1b8d66966668452019fb99181907d93c4c560edce242b.tar.gz"     && echo "9045a697728eafb7c14d20a4170b7906c2f813b55a5bb32635f1963318df140c  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:00ee01a8a4f0d3d97470c0d349a8ee4b534ef5a20a1c1abec5e0697493d8c08d`  
		Last Modified: Wed, 07 Sep 2022 19:40:41 GMT  
		Size: 56.6 MB (56647188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860b245692459684d75b294e1d16f2407220fe53f4ae799e5a91d34fe73061cd`  
		Last Modified: Wed, 07 Sep 2022 19:41:38 GMT  
		Size: 334.8 MB (334805757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:b393108d01e77ff923d602f837fabb1aa545e8b913fbb1f7130d2ca30bde3c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c5e654f04302f2f88bdc5fe9644b7a096405205432a3738fc2ca6d4b766b6037
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62303269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bdb519be2070a170aee5940166344f2a871e7d22887366c0a30406094727bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:10c927b25ed56533d46fc4f2ac0085bc5f8839527c83ee5ea395753b019d899f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63912418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c44e7db5ae05cce1a4890c4507b657d00a595765e478417de6cbe69d4d4eb01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:a4a7095f6cae0281cf3a5f357eda5174a0e2ee3fb1f584858f2740c0958a7eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f1c531eaf600c693158c1d1ebbead9146809d78fab280d8bb9fa3b255b8c5af0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.4 MB (486378202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1900d5d0b057d3ad0be96c67ba2666b4016b5a9e87c34e4442e61d12d4002336`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:19:40 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d7c2b2aa50fe3ff7023a3909084d659b7f234ce37cb2b8a54bc449bb682a27`  
		Last Modified: Thu, 22 Sep 2022 19:20:48 GMT  
		Size: 424.1 MB (424074933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c64709a723326277e8bd139dee26c099248a5cfdc15af39276fdab5bfab370e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487987310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e561a7921606d2497a6dd0c931d14e2c4efc3c741a9a665cef47c145e63222`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:39:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366907dea1a523b535578b50385542ee460f0d786719b57a5b8a57f84d86c59c`  
		Last Modified: Thu, 22 Sep 2022 19:41:14 GMT  
		Size: 424.1 MB (424074892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
