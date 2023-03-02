## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:854037bf6521e9c321c101c269272f756e481fb5f167ae032cb53da08aebcd5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:b2175cd4cfdd5cdb1740b0e6ec6bbb4ea4892801c0ad5101a81f694152b6c559
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f2314a03de34a0a2d552b805411fc9553a02ea71c1291b815b2f645f565683`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:38:47 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:38:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:38:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:38:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:38:48 GMT
ADD file:fb4c8244f4468cdd3f666932f05805a3882d34010d3a0c14b7c20589bf619a9c in / 
# Wed, 01 Mar 2023 04:38:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:76769433fd8a87dd77a6ce33db12156b1ea8dad3da3a95e7c9c36a47ec17b24c`  
		Last Modified: Wed, 01 Mar 2023 05:41:12 GMT  
		Size: 29.5 MB (29533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7f1627151f895be9f4805b8a092f0d17a3365c142c95d44f9c857fc891172fa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26137949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b861da44337925963eb70b8671950999df7d8abfe7f5a9b5f95ff9f4cca7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:40 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:43 GMT
ADD file:12d2a7ddc8445b8f97c960075216eb8e8cd226b84259c7343ef15c65a440b500 in / 
# Thu, 26 Jan 2023 05:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:860e874323ae800886f85ab5c346783e3a9371bd9beb72c5f25e8e20c9dd18bb`  
		Last Modified: Thu, 26 Jan 2023 05:14:09 GMT  
		Size: 26.1 MB (26137949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b885cc8d4c735d3f407f4318c7ba917f4d95e90599238b25705fa0052490216e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730eeb702b69e53ae1c79541a48af6303d1bd240014dc6b4208ee4f3fab7b681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:47:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:48:01 GMT
ADD file:cf91de9ab30abab112d58c0a7f3bbb35853a02b2e406c65c89430ff049573c47 in / 
# Wed, 01 Mar 2023 04:48:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0a4bfa485d176c141f6b88493559f4802a12bdeb8249869bfc276bc48a3db35`  
		Last Modified: Wed, 01 Mar 2023 05:41:24 GMT  
		Size: 27.3 MB (27347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e16a2cbc79944bdc4ba343cb4c8122b2df63ea1ed9ff3d7d1b68e69de10839a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34593768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0839ad886190c004a34269c256fee12363dbdeca9a6bb037f641189d3671d98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:09:57 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:09:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:09:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:09:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:01 GMT
ADD file:e4d45fbda8cf3ca1613a11d2b929670e0e12b43c66818636afa9ebcbf6b48b59 in / 
# Wed, 01 Mar 2023 05:10:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:477676dacb828b00e0bd0791d7b4ff0c78a073d6945e495f12acfe6df21390ac`  
		Last Modified: Wed, 01 Mar 2023 05:41:42 GMT  
		Size: 34.6 MB (34593768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:5bbb1acb9a1f9fb70ab89aa70ad4ca9683719ed0d6d3a88a429c1c1c9c86b1bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28015900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b171e9c3baa3c3faca501ce7e4c65889216978c0ca1836bc1a9d9400fb71f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:10:39 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:41 GMT
ADD file:db14dc9a9d330115a6699be3c4a344f5fe366ec17e7d3649c4ecb2711605e52b in / 
# Wed, 01 Mar 2023 05:10:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:84342823b8c9656558d3661e99cb03bf0ef7d2a83280a005cac0109d6ea85e16`  
		Last Modified: Wed, 01 Mar 2023 05:41:48 GMT  
		Size: 28.0 MB (28015900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
