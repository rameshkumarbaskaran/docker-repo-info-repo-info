## `photon:latest`

```console
$ docker pull photon@sha256:839f81d0fb0ce9bf8a68dd9e89852470b4615ac25796cc8072516a6b950ab140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:05ba9bdac556e374410e90a0a90325121f29e80aa63f0a7ce742c43dca305439
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27a562094207a2c19e5279c06cc81fa52fee37a7e627676646a9cfb6fbcacd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 May 2022 22:45:31 GMT
ADD file:67341691e9462bea59f02d5ecd96cb12060aa8aee607286bae437db1f4c0c40f in / 
# Fri, 20 May 2022 22:45:31 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20220520
# Fri, 20 May 2022 22:45:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:952860b5285f474d869e0cd1319d2f6ac3369288ea58edb77910a4be3c123210`  
		Last Modified: Fri, 20 May 2022 22:46:12 GMT  
		Size: 16.0 MB (15977432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:4c4837792b259b73b40611c679150f576e6c2666ef5f4f4f3a71d56588a952b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15049029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9b4a2af563c6bb26d37691da6142c64b1ee3ce12303926d74ff420d86557c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 May 2022 22:32:27 GMT
ADD file:2f903ddbaeb0adcaed73557189e79bc69eed3da162bf7efc882d056dba5979d9 in / 
# Fri, 20 May 2022 22:32:28 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20220520
# Fri, 20 May 2022 22:32:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:34146ac38427718c4fde42a5ad38d5d4fdd29fbce216495b0332a1f83eb8cae6`  
		Last Modified: Fri, 20 May 2022 22:33:01 GMT  
		Size: 15.0 MB (15049029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
