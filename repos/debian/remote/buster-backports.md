## `debian:buster-backports`

```console
$ docker pull debian@sha256:a7a1de1861ff9acfe976a4cda09ff40c4b6d9aa2349f1a2c348dd6261f35018f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:5cee24386e991d71612ab6603b2aff208c27307120244f056144a829e75e1c95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50448964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772a8bf029bb6c561bca9f7fb1b0946ea1bcd183340c2045e1dd1c91c02a5643`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:34 GMT
ADD file:2fa5242038736e48eaca794d061079c1cbd32fcc4336250001523c41b3177276 in / 
# Tue, 04 Jul 2023 01:20:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:20:39 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8eb6dba554cffc072c7a6c696c8a23fc311e543399d84ab3ebc55c07ab54414f`  
		Last Modified: Tue, 04 Jul 2023 01:26:01 GMT  
		Size: 50.4 MB (50448743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73104bcafd56465a15bf1dc7a6ee33d7f91692b9f20f0dd8a535d1d85d480d37`  
		Last Modified: Tue, 04 Jul 2023 01:26:13 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5b5a775a224016909354d484cdfd5367605b51e79bf2a136efd22916ab868ee6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fb2b4ea95237b03a7b71ba22054a5d39756dc5eb23ce1ac5b5a9f75763047c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:31 GMT
ADD file:e1c7c10335e2ac86eba02c2785d0ff530cba87131e91c42924072b4010418f93 in / 
# Tue, 04 Jul 2023 00:58:32 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 00:58:34 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b19cf971d5ed51e0bba0bd71ccd7b797ad4873a62fee0f49588f6ef19a58e659`  
		Last Modified: Tue, 04 Jul 2023 01:03:55 GMT  
		Size: 45.9 MB (45916488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d7a9a6f5f8af9bc7b70d526883758c669829e4729676cb679627d37198c4a8`  
		Last Modified: Tue, 04 Jul 2023 01:04:09 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7a0ecca18790e4da06afa198c5205e35d0468e2584b9aeb7225ccb295a1f25be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49238868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5838c8e457b798f2dfafa204263242d5c9f5a32456b0a0e16ef1aebd2fc9eac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:59 GMT
ADD file:a61276f534601d7b193af24e35c16b73a2913511d2b1ad997c9a8cb907685257 in / 
# Tue, 04 Jul 2023 01:58:00 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:58:03 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5e2555ae6edde2e7933c533234cb224b6d7ef3a3c90041851e31fe29ab7197c9`  
		Last Modified: Tue, 04 Jul 2023 02:02:18 GMT  
		Size: 49.2 MB (49238644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bd34674a07551d61f9ca8bbd42e5eddcf7a519a3b1e5f8c9bc38c0cdc6192b`  
		Last Modified: Tue, 04 Jul 2023 02:02:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:535e1335439a5db5cf391762a69bf2b785df7a464db005bf9a165849ddfdbc07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51206500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96aeea16dcce4187c28b7ca7c004bb761002bafe12ae4baf50bde091640f2d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:39:11 GMT
ADD file:6ecab94f7cb2bc0740a669cfef73f0837a2ecf6475dfb0fc072cbd1a7f60ec41 in / 
# Tue, 04 Jul 2023 01:39:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:39:14 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9b3c3fd2dd1697ce9fed8a2be0142b2d1294d424c56d0ce6d44bb8055d77e35d`  
		Last Modified: Tue, 04 Jul 2023 01:44:33 GMT  
		Size: 51.2 MB (51206276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddf80dc1aef027de6ef3d70f92e50550c771984d2208d58d8135bf73c589736`  
		Last Modified: Tue, 04 Jul 2023 01:44:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
