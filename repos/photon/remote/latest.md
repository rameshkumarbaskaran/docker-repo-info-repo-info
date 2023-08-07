## `photon:latest`

```console
$ docker pull photon@sha256:320e841b8b03d7ee9dd9f9d7200ee9f3ed1a5cb51d765af7ce728f061c6759ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:90d1ab556277901a8689e9703a6ef13467502b008963641a4c64a914e6b40f29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15922856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b2944aea33ad7d1ba869899f445c60c3841da641efba33a6fddaab838f3a16`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 19:34:26 GMT
ADD file:df639de0210dbe87d35120762857e9ffc98fa270779743f006deb6b233bc919a in / 
# Mon, 07 Aug 2023 19:34:26 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20230805
# Mon, 07 Aug 2023 19:34:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dc1f2e1c51d8659a5f13b47fe5ac35729f9f2c25e5de0c8add8dc05bdcf147fc`  
		Last Modified: Mon, 07 Aug 2023 19:34:52 GMT  
		Size: 15.9 MB (15922856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:c7f0de77d81ffb4f09f5286a85bfddbbc0d9af91cb70e21255270b3c923560b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14928224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d433917373e63e20f1d56f4feb7c081c9ca2e5e81ce20e097680cd14378a2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 19:45:28 GMT
ADD file:b7da30132288f4797b248a46963dee789f2331bd49986e3caaec926ad42bf351 in / 
# Mon, 07 Aug 2023 19:45:28 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20230805
# Mon, 07 Aug 2023 19:45:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d23f290101d14fd5fd3e6c282447697e2cc662f3e9dec329a35005ea3081099b`  
		Last Modified: Mon, 07 Aug 2023 19:45:51 GMT  
		Size: 14.9 MB (14928224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
