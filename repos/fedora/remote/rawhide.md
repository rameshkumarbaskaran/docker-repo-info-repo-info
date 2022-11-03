## `fedora:rawhide`

```console
$ docker pull fedora@sha256:5c447cde12b0ee2e2add6bb9a1d4f3170a65cf1dc09ac95f2fbf8b50042d2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:c7dfa518d9db440fb02362c0f9b014c0e1b8e04bc0f6bf540d1d5ac2ecb43453
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65568074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b902325de1ec96bbbeecd610ef5dcfba06da72e6831eb0ac1049e376d7778a58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:41:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 03 Nov 2022 20:41:08 GMT
ADD file:aea454c4f9f7bccbd03cf61c6477deac629e6b63f8ef39d87667ee4efaf12136 in / 
# Thu, 03 Nov 2022 20:41:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7658a6d4e9efd0ec04b7aca3c754f4441c79d4dedab19a67c5f5293bb0b5e151`  
		Last Modified: Thu, 03 Nov 2022 20:42:25 GMT  
		Size: 65.6 MB (65568074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:b4fc674566ca392e7117508f46519362a53f2c32147cbe8ae6e59a7ebe8b93be
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (64007024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e8e907dcbcc2c2b343c0c9bc5281dbccea310bcd3a98d2d7037e39f3929705`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:41 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Thu, 03 Nov 2022 19:58:44 GMT
ADD file:d63621367aab7d458af7e75ba42437bc50c5c9166122e52b7a46c5cea2e22147 in / 
# Thu, 03 Nov 2022 19:58:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5acecd05a9bc955b7cb9f11323f55414ce45efebe26d8fd51c2f920bdafa3c2b`  
		Last Modified: Thu, 03 Nov 2022 19:59:52 GMT  
		Size: 64.0 MB (64007024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:2e654720f503e00a51896d0bbf6be86f5a4cdc74b8af3b15df754aa119338adc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65082437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ce470833537fd2e5edce21188b4d5d38fab63351bc3b631c456b7923ef6d0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 11 Oct 2022 12:17:51 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Tue, 11 Oct 2022 12:18:02 GMT
ADD file:f7c6a76f76aa4f0057ce16cf3e83d5b5c9296ce5b33995dc1208bd2b4fcd7548 in / 
# Tue, 11 Oct 2022 12:18:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:214a5de1153fd8724f8adb4d6b525ec50a5139f2e6a0736d609d21d66ecc9f16`  
		Last Modified: Thu, 12 May 2022 22:32:43 GMT  
		Size: 65.1 MB (65082437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:8a746cdc3af9334bcbf48be4bebfc6d6428af817e6e886b26f495b718c666911
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56500892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69f754d5d0de1955e685cf252d714b6acc593b9ced3f6a106958ca68c64d50e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sat, 19 Mar 2022 04:31:50 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Thu, 12 May 2022 18:43:48 GMT
ADD file:3f10131e3bc0caa9a0206a822c9896790eac5b35bf4ac1accb5652f1cef842ee in / 
# Thu, 12 May 2022 18:43:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1163606821de65d610cb57b7fd309908cb7b5d049fa1c4fda6773be2e54e5628`  
		Last Modified: Thu, 12 May 2022 18:44:39 GMT  
		Size: 56.5 MB (56500892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
