## `photon:latest`

```console
$ docker pull photon@sha256:2740f7f0db17c70ed480f493726ad4cfe586d9e0a605d6b45178318695a05165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:cc816b7ae95eeddafaa377605619fcd498963594214f6fe21327c9d1f795dd66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15682685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e2b5d9faa30ffc998ca8e3d76868f7c1dd3f57e06d5ff7b3000019dbbbd22e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Feb 2021 20:46:35 GMT
ADD file:050ee8c7474d278ac5a12b52720530737972106318aeccf4de27f861a087de4b in / 
# Mon, 22 Feb 2021 20:46:36 GMT
LABEL name=Photon OS x86_64/3.0 Base Image vendor=VMware build-date=20210219
# Mon, 22 Feb 2021 20:46:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3ade12ebc8a53602a8f252da3b59d96dc7a2d0f219ba832b38db55f6d1a96b9d`  
		Last Modified: Mon, 22 Feb 2021 20:47:23 GMT  
		Size: 15.7 MB (15682685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:70ad3385c855b0e86676c26255f7fb36654a5034dceb28ca6185f712fdb04fb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13443597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7f0db3a1693b6582562a530cf33c4ecbf4a56af6ea9dfe478fddd1d731b446`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Feb 2021 20:44:49 GMT
ADD file:435cca5a4fcbba566cddc781020dcbacef3e29a601fe27b8d57f9479eb40ed3b in / 
# Mon, 22 Feb 2021 20:44:50 GMT
LABEL name=Photon OS aarch64/3.0 Base Image vendor=VMware build-date=20210219
# Mon, 22 Feb 2021 20:44:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:877a8ed7895bf309e3bb975af42d0289c1a72ef8517f048d2f468451cda3e8fc`  
		Last Modified: Mon, 22 Feb 2021 20:45:05 GMT  
		Size: 13.4 MB (13443597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
