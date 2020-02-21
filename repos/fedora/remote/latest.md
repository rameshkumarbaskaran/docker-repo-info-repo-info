## `fedora:latest`

```console
$ docker pull fedora@sha256:c97879f8bebe49744307ea5c77ffc76c7cc97f3ddec72fb9a394bd4e4519b388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:d3d106e8f3affb1011b97c2b6ef388430dc1474bf7c7ad05963cff49961edb89
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66666475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536f3995adebc20891c7b195832143611fb173807b265005ce38d028122283d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Jan 2019 21:21:55 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 27 Sep 2019 21:21:07 GMT
ENV DISTTAG=f31-updates-candidatecontainer FGC=f31-updates-candidate FBR=f31-updates-candidate
# Fri, 21 Feb 2020 02:41:09 GMT
ADD file:a9b09cf691b5509106ab840a442628e5b3a422dae698fc06d1bd5c914d219497 in / 
# Fri, 21 Feb 2020 02:41:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c1b9e8d7bf7b758fa84807a6bce45e4af333e1ddd566b5972550b6fcfbed9b8`  
		Last Modified: Fri, 21 Feb 2020 02:43:15 GMT  
		Size: 66.7 MB (66666475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:b0d24e01fbfae9b54d27ea1c56aad451d7eafd58aa0174d578dece0ec91009cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66535521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a50f9110d4e2bee94a42cfa3c8ce88ce7dd73631cf2f590dec1063aabe97c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 27 Sep 2019 21:41:10 GMT
ENV DISTTAG=f31-updates-candidatecontainer FGC=f31-updates-candidate FBR=f31-updates-candidate
# Fri, 21 Feb 2020 01:00:36 GMT
ADD file:802fd23d2e88228881203b44c1e64bb1fda52436fee03fc94f0ed37f77d3bccb in / 
# Fri, 21 Feb 2020 01:00:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbad5a3d9e059ad673cb03431604f7d02d3d16a4f6bad97eab35b8db19259d0b`  
		Last Modified: Fri, 21 Feb 2020 01:03:05 GMT  
		Size: 66.5 MB (66535521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:a14503287b17ff0973c5c14b5b314541bc28e285a1aac40a5a3d8321306605d2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72435603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a2e55dc4bd0b06f6cb156457dc638d79a4f6763f9211446557ad8d8f724bdc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 23:19:06 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 27 Sep 2019 22:08:22 GMT
ENV DISTTAG=f31-updates-candidatecontainer FGC=f31-updates-candidate FBR=f31-updates-candidate
# Fri, 21 Feb 2020 02:11:31 GMT
ADD file:8c0894365604553c22e31d7b8300e196c0394e3e7a5612f04721bf6cf8460596 in / 
# Fri, 21 Feb 2020 02:11:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8e7c371b073340b1b6031368ac38714735285c0b94d1a972357562888c5ad607`  
		Last Modified: Fri, 21 Feb 2020 02:13:45 GMT  
		Size: 72.4 MB (72435603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:df186480927cc4fdf9d8350b255fedb98e48cbd2a3a6dca794523f62f2097e3c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63903433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044f7646c1c935b31f40c8c3f31c5f124be36ca95e6ebaed63e5233a1caab206`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jan 2019 12:43:09 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 27 Sep 2019 21:42:39 GMT
ENV DISTTAG=f31-updates-candidatecontainer FGC=f31-updates-candidate FBR=f31-updates-candidate
# Thu, 20 Feb 2020 22:43:17 GMT
ADD file:c567f902e775272a4a040d6f191cda1bdb8e3589b295e8bd90535099ddfe82bf in / 
# Thu, 20 Feb 2020 22:43:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6decbeeaf87b7738a70081478c58cc225d73039e15a07e51f6d43236e23f5649`  
		Last Modified: Thu, 20 Feb 2020 22:45:16 GMT  
		Size: 63.9 MB (63903433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
