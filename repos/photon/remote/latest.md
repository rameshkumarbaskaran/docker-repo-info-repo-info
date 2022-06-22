## `photon:latest`

```console
$ docker pull photon@sha256:b0ab8342a3cd058188cb3020a567f9f26475a125d1293060949b7425ed56cda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:93e78d29ec0251c0d17a75b67517723be46415176069d3ed6e5f53a451905ca6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15994650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac57605758da2c1cbe70dbb0cabcbc224c9d5807a251cebe3cc3aedd289af15c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 21 Jun 2022 20:29:34 GMT
ADD file:b3821b901bebbc71d96bc15cc85dee3668b218217c7af07a4ce59f19d4a5c37d in / 
# Tue, 21 Jun 2022 20:29:34 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20220617
# Tue, 21 Jun 2022 20:29:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a7be428180ec08030a24b399f52c1af25ff48553185409b45a1eeb9720ab2675`  
		Last Modified: Tue, 21 Jun 2022 20:30:10 GMT  
		Size: 16.0 MB (15994650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:d6cedf0860594e5e812e85cbece38feaaddde0201e3860020bb796dd73fca838
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2908b10f27b14dc6e624397789c8b046ffa0a2b8cc4e7eefd48c4d509401f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 21 Jun 2022 19:44:06 GMT
ADD file:9580e26aff704f08705c165e7c33534c18cd82defe15f9637d936bb6d9155b0a in / 
# Tue, 21 Jun 2022 19:44:06 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20220617
# Tue, 21 Jun 2022 19:44:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f9a7e8fdca06c05f293d0fab511d8918cbdd4679c019de7b1be6d151b42caa79`  
		Last Modified: Tue, 21 Jun 2022 19:44:36 GMT  
		Size: 15.1 MB (15064304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
