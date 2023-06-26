## `photon:latest`

```console
$ docker pull photon@sha256:95ced744d56f30f9dfcf8d09d0fa7af035610dfee8e62e3d16c3712eb0de9edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:9dc3575aa7f0b7f90ba903d1a729626c903766033a7927df6035e136d3c5298b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15915940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7a3ba8cfd371c1015a87a792e56be5e0fd84764d17c29c6ca1bd4e677780b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jun 2023 21:20:49 GMT
ADD file:5534e22cfb513d4ff9bbf4589d70e2202b93c38a18498b5b8d54116e518d2ce4 in / 
# Mon, 26 Jun 2023 21:20:49 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20230624
# Mon, 26 Jun 2023 21:20:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e316eb2a8fe9c65525bb37c570edd1515ae3e4f25d29b4ef7f1e3646d6a4f1c5`  
		Last Modified: Mon, 26 Jun 2023 21:21:12 GMT  
		Size: 15.9 MB (15915940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:80d0de30ca8dd2ba5a75672023a3f132dfc0555322b5604879c20cb0ccc21338
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14913402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9294883aa92917f960c408756e226e280b62cbeb672b96d21e7de8dbd7f410a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jun 2023 23:04:36 GMT
ADD file:15a5f8eb08a55e9f936eaf6ae91e06e4789a45a722c90daa3e8dcb7d8041d402 in / 
# Tue, 20 Jun 2023 23:04:36 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20230619
# Tue, 20 Jun 2023 23:04:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4a1b4214e9585e2b2fbf120aee7ead44ec41d771f2dcb8ce867b18c19f7f4f81`  
		Last Modified: Tue, 20 Jun 2023 23:05:00 GMT  
		Size: 14.9 MB (14913402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
