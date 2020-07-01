## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:cabd4899d925930e6492d4e7cb8ed7e2fb369e03119a834b072c43b71f348c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:420d5d3cfb86d4e124377ab32bc6f9e1504a07d63c0fff4282c49aa7c436c9ec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.9 MB (476922148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80a4bcf0ffd4b139a9c3d2390bb8b6aa5e6b6aeecef63d6934d908bcde98229`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2020 20:20:29 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-9af89b3a0cae0f976ef3a0f7b0a0568f88bb8a6a99cb0b19d4c75a7af24fdd7d.tar.gz"  && echo "3d1d16d828b58c8855a5899401da4cbf47e3096cbf2bd798d9a690b9021e2326  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b36c1db94ea96b1c9c9ff14be0be653f85063ac10bae9324bc5545309ee7fd`  
		Last Modified: Tue, 30 Jun 2020 20:22:34 GMT  
		Size: 415.2 MB (415237466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:89428213350981feb89f90d3d9417e2976391753480a3346dc1fe4a42ea8d250
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.4 MB (478401288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a630e3503fb5aabbc497b6e5973256244ca6d91ce3962264478679c2e709cf5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2020 21:59:48 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-9af89b3a0cae0f976ef3a0f7b0a0568f88bb8a6a99cb0b19d4c75a7af24fdd7d.tar.gz"  && echo "3d1d16d828b58c8855a5899401da4cbf47e3096cbf2bd798d9a690b9021e2326  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04069174b6fe5d0ab7681b352a7509678c8561b0fb6c1c9aaeb0acbca7da1d67`  
		Last Modified: Tue, 30 Jun 2020 22:01:09 GMT  
		Size: 415.2 MB (415237506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
