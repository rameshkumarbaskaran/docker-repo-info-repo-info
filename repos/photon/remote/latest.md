## `photon:latest`

```console
$ docker pull photon@sha256:4cf2a1ce0a3f4625f13a0becb6b9bccfdb014c565be6e9a2ec4c4aad1ff8a5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:1b0d90353bd99cc16c24662a89a1a5bd4d31309dc0d8393f974fbaa15613beba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15922845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176b9b7c816e414648afb18af610b1af85c10f49c50f4a14b7b74d481b554bfe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 21:20:28 GMT
ADD file:fadc402f84e1d5c814507059567da6b0e6754e6b0e0bbd041b19f2f869605a0f in / 
# Mon, 31 Jul 2023 21:20:28 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20230729
# Mon, 31 Jul 2023 21:20:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:549f5d667deb3c7c555273adf34aef5a27841ed11ddbfbe27bff182b711ba404`  
		Last Modified: Mon, 31 Jul 2023 21:20:55 GMT  
		Size: 15.9 MB (15922845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:f980c1cff252c20fb506a3f04105853f334df85e5cecbf9b982117690ef8f5e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14926602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a49b4e6ea7d042b9cf87f489ec8482d97502bbdd18f4845348f9b1d0278c359`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 22:03:39 GMT
ADD file:fe99499a06f5c25d5c24895b5a1e19ea6703a49f823d7999821c93d83a5b414d in / 
# Mon, 31 Jul 2023 22:03:39 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20230729
# Mon, 31 Jul 2023 22:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:79bad54101cde362156f814c2536d3ece6e4ab0c6a777b45b50cf78b9dd8f59e`  
		Last Modified: Mon, 31 Jul 2023 22:04:04 GMT  
		Size: 14.9 MB (14926602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
