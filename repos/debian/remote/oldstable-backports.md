## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:7be6b06637510ab33c39482e0145d77bd2f536a456a2bf6eec6d891034bc3a9a
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:0e15601f2bcc351fe96c59ddcad6bd1588a525a8dcf2b2466b630712b85c8288
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50438180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9418164fe1887ed2f941404c75eeb20096223c32dbbf316abd08f50029693271`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:21:06 GMT
ADD file:8feca9d28a2a8d6126daec12998c85ff78e935d64bc69fbea9fc619031218d02 in / 
# Wed, 11 May 2022 01:21:07 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:21:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:121ac68e5d46421809718fa673b83e12dab2f7f5304f1ec020d8d071520ffc52`  
		Last Modified: Wed, 11 May 2022 01:26:52 GMT  
		Size: 50.4 MB (50437957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f7867544b043b157b84fac080e386b2ecab866532309593545d269dc446a1a`  
		Last Modified: Wed, 11 May 2022 01:27:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:315a6620251c0d8971415ca776844472a2c76c48094ad85ec36af949d331c2de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48157746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a491c68c6586cb44460c16bd98e93d2e80f3a73fcc05382f478179a370c274`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:52:55 GMT
ADD file:52714e05eac3ec4a580498eece5bc04180a97c91db34b5f384ad4269e59ca287 in / 
# Wed, 11 May 2022 00:52:56 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:53:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d34300cf0b997d5df249ea70a7fa8dedc9c567168af6538af7d2bf1f6a0e2f4a`  
		Last Modified: Wed, 11 May 2022 01:09:20 GMT  
		Size: 48.2 MB (48157519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bf94ce32e17fc2fd6d028ad76b949258e94932a25ca2eab0e18aa18d4e1228`  
		Last Modified: Wed, 11 May 2022 01:09:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ce71e54359a3086262197b78db1974e9ec6896c4e7b9f59116d40daf0221f446
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45910419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342046566dbc00316e633a6237d2157f0ca4cf7121f7cdb409900f94202ee5b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:51:42 GMT
ADD file:bc23b97fd6c65c5c3801548bc21a9307787fd43f930ec52544d47715e005ed79 in / 
# Wed, 11 May 2022 01:51:43 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:51:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cc2fa3cda1ed31d10ab5b045cba773f39f43692685819c78f936576e2e072c89`  
		Last Modified: Wed, 11 May 2022 02:07:50 GMT  
		Size: 45.9 MB (45910193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ea8b22c610a1c24a9c31384c01c3de30c406d21ed7530890ffe8ee25471813`  
		Last Modified: Wed, 11 May 2022 02:08:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:304123c9068078b07f8336d1fd737aff2755441d2199956a44ec062fefd2b5bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49229262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df8b745e46615134b1293feda6c50b33c284834775451b7ce9a0e0b4227ebe3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:39 GMT
ADD file:80d27c6c157fd32ac9b69d8d7115259ba021ed0d7447c50aec7251a3899b4b9f in / 
# Sat, 28 May 2022 00:41:40 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:41:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:08bc7b3927bd8e671ea9952e215bb10105ddea98cf2b83651a3cf922566aaee0`  
		Last Modified: Sat, 28 May 2022 00:49:28 GMT  
		Size: 49.2 MB (49229037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a049f923c4fd9744c9915898a0ad7eb06d9521d521629115c654090e316c231`  
		Last Modified: Sat, 28 May 2022 00:49:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:9ba251d25455c11c00d554a7b4ae4518b58ee133097199c62ad85a25ac2384e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51204449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b66af000d0e5c27ff1e0fd1c87c01de3e88cd593cd3c11de19c187d8242ad6e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:37 GMT
ADD file:1db3a01981cc79d71fa5a24eba6c14a72990ecc081ed01b6d41e493b63e95ebe in / 
# Sat, 28 May 2022 00:40:38 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:40:44 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5559dbed49d2bf17fd15cac89e8b285b3d786020b52e88da8688c6b99f993d24`  
		Last Modified: Sat, 28 May 2022 00:48:36 GMT  
		Size: 51.2 MB (51204223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f214f4e5e3c12689fe4c306a8e4323a8323d78242950c734f5633546831758dc`  
		Last Modified: Sat, 28 May 2022 00:48:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:69feddf1306f18fceea49db6fd151e7e10435c18b8ec59532228c78f160efd24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49074015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5038da7be014f28533d572b367cdb6501b7719157823db5b0d824e9a1df72ebd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:25:15 GMT
ADD file:178e9c4ae0ba73a39c5b219aac7fdf90947e85dfd216f3e6cc755689cb94d01f in / 
# Wed, 11 May 2022 02:25:20 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:25:30 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:530ea5816183e6df78f38b719ae529269973d546d9dfd2215ddc097166ee82ba`  
		Last Modified: Wed, 11 May 2022 02:35:46 GMT  
		Size: 49.1 MB (49073789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438a8be483fb6f9cd16e1ec74e49d785d1a774a59c7266f7c39f3e7491748959`  
		Last Modified: Wed, 11 May 2022 02:35:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a6a18d55340c19a736cb2cf9ce4db66f1ee0b9f04b9c99040c05eed89fd6bc58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54170446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06944a714791d50b91aa20ce9883a7842a4ea7a1706cb200e3b3c3a5e3e55c83`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:33:56 GMT
ADD file:d94963f087ad2000194535dedbddaabeb9aad13ec17d2be7cb40a10331518cb1 in / 
# Wed, 11 May 2022 01:34:06 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:34:29 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fb1dbf946a84c7b646db97d3a663ada35dd5588d1a1df869dd21916fa072de04`  
		Last Modified: Wed, 11 May 2022 01:44:35 GMT  
		Size: 54.2 MB (54170221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465313426012f74e86973acc5f0d93cf319729015129d687767f25fc5a67f5d9`  
		Last Modified: Wed, 11 May 2022 01:44:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:6be4457287dc2975ab5809d5bb1fd67411dc2b632474fcd510f1c471439684ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49007014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5a713c73f7dcf337bffb30a2c53cb8dc8561defbeb66ef794750568bdf1c6a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:44:00 GMT
ADD file:bd5cfd4dc8d90cc91b330c8c19624771c01f1ad03a3a3ab3cd71cfb76d2dd66c in / 
# Sat, 28 May 2022 00:44:04 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:44:12 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:97c6438ef1df635b92390f341cba00358af65b7c27e2bd11a4ef6fff81d5a77c`  
		Last Modified: Sat, 28 May 2022 00:50:36 GMT  
		Size: 49.0 MB (49006790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e018bf5713abbf9d45181c0fc3d8ae96bd8af4f9ca470229efa053079e601877`  
		Last Modified: Sat, 28 May 2022 00:50:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
