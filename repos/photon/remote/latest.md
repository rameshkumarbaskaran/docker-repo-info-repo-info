## `photon:latest`

```console
$ docker pull photon@sha256:1b2721e7d8ecceaffbf990c23d95287eadee9632d223983b4b4f5ca4a861e4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:89df4660399910ab17781d1ebe619bf91c53326e4cc039ba14228b274510e344
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15924653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bf7edd61c6bdd38317f3419876e4ad23b0098192bdf199d3c92263cd2321dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Sep 2023 18:19:59 GMT
ADD file:68e2e1a532a6586ee95b7a5243415e13ff8ceac430af17748b43a2061cfb0e36 in / 
# Mon, 11 Sep 2023 18:19:59 GMT
LABEL name=Photon OS x86_64/5.0 Base Image vendor=VMware build-date=20230909
# Mon, 11 Sep 2023 18:19:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9237c7978d1801f7cb4b7f1c3daef0adc9a84ad96258aaa69fc0c450baf6624d`  
		Last Modified: Mon, 11 Sep 2023 18:20:23 GMT  
		Size: 15.9 MB (15924653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:195a8f6d2ac70b53b1c677f96cc1a288fe066c20750d04ef785d1506e049c6a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14933071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421b58d8a66931a856bacc18634458edf67e37e7aa818539bcc5b2f706543e02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Sep 2023 19:15:05 GMT
ADD file:535a0f1fbf58e5bb990692e07cce58382f6338790da5d976c830ba7ea3cd0dc5 in / 
# Mon, 11 Sep 2023 19:15:06 GMT
LABEL name=Photon OS aarch64/5.0 Base Image vendor=VMware build-date=20230909
# Mon, 11 Sep 2023 19:15:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a1258da419d214738d3f92b5f838d48fc07c237745204d853e21fbbb1229880e`  
		Last Modified: Mon, 11 Sep 2023 19:15:25 GMT  
		Size: 14.9 MB (14933071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
