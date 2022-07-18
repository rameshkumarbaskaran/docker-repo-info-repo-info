## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:b3d7163b49e34fed2448cb3194b72da817cfe2668a50b829f0a0ad0e8f909ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:0da8d43607b99cd911476ccf348494d5ab1dc35eece545b93ecf8ae0bfc6c2fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.3 MB (483310117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc59403ca82d1151dc5350ff49d1f46a02570c67476d1827e77f3ffc00be3e33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 18 Jul 2022 18:19:51 GMT
ADD file:75b27ca39ab75fecc055b0d9cc3cf3ca2cc4eda970f07d6b4238d817c796f5ad in / 
# Mon, 18 Jul 2022 18:19:51 GMT
CMD ["/bin/bash"]
# Mon, 18 Jul 2022 18:20:16 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6ad9d68b91be6ac7e867c110accb52ae5eea9db45924a4ca3d4d32cde09c2f0a.tar.gz"     && echo "70a0d5140609568de4135eb7074409d868e13d33b0fceeca6e06ba401cf47f70  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:bcdbeae41a50412a643b551338b505ebbf6e82c88d6905f583f8a7f6c643142d`  
		Last Modified: Sat, 16 Jul 2022 04:16:46 GMT  
		Size: 68.8 MB (68803613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952eb23d7b2922e0bf82be6a85d48b715a54d5ae782f108a8e3020961081f214`  
		Last Modified: Mon, 18 Jul 2022 18:21:24 GMT  
		Size: 414.5 MB (414506504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:241d31e6ceef519880bcdd19a203c569b2ca35e95483660b6dcd8aa38e12b4d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.0 MB (481983659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748231095de7ce3c656cfc5664207291ea55b54726e4d61a7baf421e018b8f0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 18 Jul 2022 17:39:42 GMT
ADD file:00537eb2d5579c8983266ab7fe474cd529f7015e22ac65dd87541e46b0d04efc in / 
# Mon, 18 Jul 2022 17:39:44 GMT
CMD ["/bin/bash"]
# Mon, 18 Jul 2022 17:40:06 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6ad9d68b91be6ac7e867c110accb52ae5eea9db45924a4ca3d4d32cde09c2f0a.tar.gz"     && echo "70a0d5140609568de4135eb7074409d868e13d33b0fceeca6e06ba401cf47f70  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:a409f18bc031ea68bf438f175b290c5730af908a1f5eacd4d3ed628376ef728b`  
		Last Modified: Mon, 18 Jul 2022 17:40:51 GMT  
		Size: 67.5 MB (67477196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ebb50bc68ff064c69dba9f8a55ddeace2ba2b508f32cf6727a987d16d4c479`  
		Last Modified: Mon, 18 Jul 2022 17:41:26 GMT  
		Size: 414.5 MB (414506463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
