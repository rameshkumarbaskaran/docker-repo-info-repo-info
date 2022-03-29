## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:c141585a856526b0a92a5b0c650ed5e52e59090aca187647c5d271036b9c0caf
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:f41857f8cc1190af14ab7e7c3ce343d53015c0d88e243cc38e28256584a50d7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54937935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aba146ec93f9f43b72149ef11dda4692d67594df05b1586b5e2a126c3bb3b79`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:07 GMT
ADD file:e8d512b08fe2ddc6f2c85831c73e4c72b9c850fa428913d19da4bb1a34f84cf2 in / 
# Tue, 29 Mar 2022 00:22:08 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:22:11 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dbba69284b2786013fe94fefe0c2e66a7d3cecbb20f6d691d71dac891ee37be5`  
		Last Modified: Tue, 29 Mar 2022 00:26:47 GMT  
		Size: 54.9 MB (54937710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e54a5b832f8ff0f20fc25edc6da8b678179279eb1455c08d3df311d36b8eb2`  
		Last Modified: Tue, 29 Mar 2022 00:27:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:48c5ea8def33265879c70e622d4e8af293b7270d693bf27961a845f01d1f7acc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52476096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c503881e5d7510692e8298831c6dbbdc617388de017732e7be3e5360c79aae8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:50:03 GMT
ADD file:6cca5eca42975074f53a45a9b4ba83d1f06b95182dd4d8d95622d63cbc206574 in / 
# Tue, 29 Mar 2022 00:50:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:50:19 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cfb93eae062e68427eb7e96f51a690313db08e4118ca20b5a644c29fecb784db`  
		Last Modified: Tue, 29 Mar 2022 01:04:42 GMT  
		Size: 52.5 MB (52475868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9387bdfdebb06136ce49cff45cae02646963626353c77237dfa4a358ed23a14f`  
		Last Modified: Tue, 29 Mar 2022 01:05:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b1489da3a3c779ab3d98583721186cb603fbb74c15e92699018ff42b076daf15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50134096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0a9bc51b0e6b32717a5929a50fdd3f38b8b90cb6a4a42346eecc63bc87762e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:17:58 GMT
ADD file:d8d3280d101d611090968c237af923598174e090c533c24bcee805d174e4a6f5 in / 
# Tue, 29 Mar 2022 02:17:59 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 02:18:15 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fc87a15f2d540adb88546a549e56aa0a378d5719bbfd07399e467a095e27d5df`  
		Last Modified: Tue, 29 Mar 2022 02:33:28 GMT  
		Size: 50.1 MB (50133868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e757f8312f44280f1b0df74caa810dc429ab2348ac8fa3c273e80ff4b33150`  
		Last Modified: Tue, 29 Mar 2022 02:33:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c67e24189e4f0f7a19c47c4f9e5a55106dfa458fa1a357fe89bf0108c9c007a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53633935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ca538e2fcb026a70b91b321362c7a5a8706a12e646642ccd745b377d9e224b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:01 GMT
ADD file:5e8f8c10da6d37a727fb5e1ed13b3dd78769f0ca7e91f0c3510e2edd25177117 in / 
# Tue, 29 Mar 2022 00:43:03 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:43:10 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fa223d8c149d7beec8e997e1415ee4961473cafaf88a932f70baf3da56f2c564`  
		Last Modified: Tue, 29 Mar 2022 00:49:33 GMT  
		Size: 53.6 MB (53633710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcb8b635f09e78412b28edc2273e8b33f467b390a1795a3c7fdbade697ece39`  
		Last Modified: Tue, 29 Mar 2022 00:49:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:9b215ae8b286b5752180103b3b8a98b8581d1c232c9e1b653273cd449170c9a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55940922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291c113e12b3687969c91d9e66c9e2d7fc4cca2ed118c36bb0ae99cdd1e9a794`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:41:45 GMT
ADD file:378357c2fb82d0ee5366dc2926393bb2779a44632ebb0b9cb95919df6d60fcc5 in / 
# Tue, 29 Mar 2022 00:41:46 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:41:53 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:861044c168563defddcd8a95bf60383713febc9f81711ebacce77cb8d8bb6025`  
		Last Modified: Tue, 29 Mar 2022 00:48:28 GMT  
		Size: 55.9 MB (55940697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a71fcfffd81a46bfb529f1d811635a3e2e9badb8646d38560b11e3bd9b2ebd0`  
		Last Modified: Tue, 29 Mar 2022 00:48:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b1d8e26633bc3bd9bcb967f20212c935870f321b0eddb5a457d41141a72f83f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53199613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f43eccaff4cdf00d92fa2a040673f311237a00de7a0a06e0ea97e9c72f81dc3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:41:51 GMT
ADD file:40fc6f06ccce55e9889d1c94556c29242d1ac62870cb9895da64d37bac45ab5e in / 
# Tue, 29 Mar 2022 07:41:56 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:42:07 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:efb90a274e1b19eec263e44f7fbc1f9c9c6c393210c27b03ebde7c2b0a2b6482`  
		Last Modified: Tue, 29 Mar 2022 07:52:16 GMT  
		Size: 53.2 MB (53199386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3607c822b6087d91a8e246d263f4d0226b8bf2237680aab28b0f5df563784`  
		Last Modified: Tue, 29 Mar 2022 07:52:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2d753d5245207925288d289b942c52ef1353e8d6c743c20636d4fe51c63d1bd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58835165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491a5618615d9c576710503d0bbb8547596921fc8946fffc2bdecfbafcb74184`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:21:35 GMT
ADD file:32dd723ee02b792cb3de67b78d352e79bdb52bf9d23fa5190ce764956b1e3884 in / 
# Tue, 29 Mar 2022 00:21:42 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:21:56 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c632eeaf13829ddb578e0545ba882dab1aee70ee0cf3069a1fc9eefd23c3e0a8`  
		Last Modified: Tue, 29 Mar 2022 00:32:02 GMT  
		Size: 58.8 MB (58834937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e07548a7d25cc571c04406771451fda91cda5fe464ed6d9b0fdc06eeb038b4`  
		Last Modified: Tue, 29 Mar 2022 00:32:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:e346af3b5cbd64caa9fbfcf08dad402056c1e47c62cc1c8d039c2980179d7ef5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53210339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9f95bd02bdf6441a6d005ea08daadf6d31eca252a14b3d45f7f7d11d03306a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:38 GMT
ADD file:3239542512469e874d06b7deba00e80df79d7544038304df05ee6484a85757be in / 
# Tue, 29 Mar 2022 00:51:40 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:51:48 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c9bfa2e596807d7800fe5f547e2f9a23f962c4657b2a6f9d9060de9104720bbe`  
		Last Modified: Tue, 29 Mar 2022 01:00:56 GMT  
		Size: 53.2 MB (53210113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7357e7b16929118eb0262a7f619ec24519653e4e7a2f07cc3254108bc24396`  
		Last Modified: Tue, 29 Mar 2022 01:03:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
