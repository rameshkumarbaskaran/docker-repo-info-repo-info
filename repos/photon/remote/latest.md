## `photon:latest`

```console
$ docker pull photon@sha256:a83ba361bbc7aea4f038c76416b657dbc91dbfcd16d152312545066cda549071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:cb3cb8a46cc56b26512e2b79b465a92c6c501108e01ca9a5481ffce95d221ec4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15776962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aae0ac8c87a4310e7c56f4286e7ddeee0d623db7ace3ec0f7761f3a1102dd0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 May 2021 17:21:43 GMT
ADD file:1a7749e42e46a7327cb9501c6973240d7e469d16e4718378a0a98d520e24a045 in / 
# Mon, 24 May 2021 17:21:44 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20210521
# Mon, 24 May 2021 17:21:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b671124209797297d0c750621375c49368c008259093e5e2246b460597ac201f`  
		Last Modified: Mon, 24 May 2021 17:22:37 GMT  
		Size: 15.8 MB (15776962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:f3260f8d9a2c68e31c9e5f361d702082e9ee16ea751c51134d96fab8a98588ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb756fcc48ad08b8d4f2db574bef0dad04d0f81bb6da87511766397c1474bbd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 08 May 2021 01:54:09 GMT
ADD file:0b86b56bb7e087afc5672440ccc1e7b695df78feb466f11c58129e3125354bb8 in / 
# Sat, 08 May 2021 01:54:10 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20210507
# Sat, 08 May 2021 01:54:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:af849382af255c1aa3a108bd751aa5a3e9fd9538d37791e5040a5f29e9fd4f86`  
		Last Modified: Sat, 08 May 2021 01:54:46 GMT  
		Size: 14.8 MB (14810017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
