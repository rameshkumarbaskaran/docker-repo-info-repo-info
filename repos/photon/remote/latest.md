## `photon:latest`

```console
$ docker pull photon@sha256:6556706666c5d8cea59202bb089e1015d59bc753a8d8b0e357bd5e9daece0c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:92d58b3d4e37f17bb158258b7060074d41417de3f4e0c090aaeb0320bc5652cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15935017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0d035dcbbfbe22e0d3dbd881011970835be67957e67585472589df21524993`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Aug 2021 02:11:01 GMT
ADD file:55b2dc748005164bfd7004d0988cdff209b7e198bc487014a95d11ab968e829f in / 
# Sat, 28 Aug 2021 02:11:01 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20210827
# Sat, 28 Aug 2021 02:11:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c993a6ff0134c17e21cbb405cbf937237dde1b8332b393f82dc342ca978f28d`  
		Last Modified: Sat, 28 Aug 2021 02:11:30 GMT  
		Size: 15.9 MB (15935017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:81fc9a4408f0763269f195e13bb73a89e174755609cb8dde7b914fcf1572adfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14979428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d579314b2538e14e745adcaf325ba62934e38c31e8ccb7917f3ae64ec238e7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Sep 2021 05:30:53 GMT
ADD file:d0e1eb08602195cddb25f231933bf1595e7822ecc9af271a45e490c0f64be8fb in / 
# Sat, 04 Sep 2021 05:30:53 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20210903
# Sat, 04 Sep 2021 05:30:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:917f1d8e71a898c84d18fee3ff4f26a5b13a1971a64840aea40290f1de6904b8`  
		Last Modified: Sat, 04 Sep 2021 05:31:21 GMT  
		Size: 15.0 MB (14979428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
