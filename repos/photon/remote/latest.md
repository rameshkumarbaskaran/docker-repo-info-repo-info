## `photon:latest`

```console
$ docker pull photon@sha256:d00aba1da12a65f93cbd68081848a14b67608aaae05f4c17475402fe5b1aeadf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:152ee27160f9e9c38b01907b6b7c13ccda2884efa399aaf3141150b12027cf0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15153117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a439892cf61626eb84b3c73e6fc45405dc9bcb1f97d83090eae31d04190c13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 06 Apr 2020 20:54:41 GMT
ADD file:c301b3b0c69adda76faf3783690e2eeb7e3a3251bc815054be344b3720100ba9 in / 
# Mon, 06 Apr 2020 20:54:41 GMT
LABEL name=Photon OS x86_64/3.0 Base Image vendor=VMware build-date=20200403
# Mon, 06 Apr 2020 20:54:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c23df2afad0e293cadaeaaf993e4305398e8c14fd3ab6536dd246f8b29bbac2a`  
		Last Modified: Mon, 06 Apr 2020 20:55:02 GMT  
		Size: 15.2 MB (15153117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:25d76ab105865deada5693c228e56ae5fc3c282c2e7af25e07fb779b0871cc0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12949841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7602766763e2993fbd81e1e8da47d317edb8a7383eff03991ac43d76689d12f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 06 Apr 2020 19:40:44 GMT
ADD file:8883f2695673a13bdfcbe86568fd7f6b73b5fbf862943f65a9f9534e29bce790 in / 
# Mon, 06 Apr 2020 19:40:45 GMT
LABEL name=Photon OS aarch64/3.0 Base Image vendor=VMware build-date=20200403
# Mon, 06 Apr 2020 19:40:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c0269f537c11928477a816177a5e6ffcec23d786f6a27cde4f691fd50e7296b7`  
		Last Modified: Mon, 06 Apr 2020 19:40:59 GMT  
		Size: 12.9 MB (12949841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
