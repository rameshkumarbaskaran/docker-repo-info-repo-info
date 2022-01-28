## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:9bf2a0dd0532389209ee16e4d89133c4911580c07d7eb01e3ed1cd6cb3b24cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:28c2b345fb8c5350946f5ace109f7e6c11db9dcfbf60e3159a2f96de39a86836
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515005681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29dcea5a92f4f38f10147976b572599d1ad45ba854e7970b6900529443342ae4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jan 2022 23:41:05 GMT
ADD file:9368a3b891d3811881ac957b51c5d8fbc62e50ac1b36e08e721877da00fcf852 in / 
# Thu, 27 Jan 2022 23:41:06 GMT
CMD ["/bin/bash"]
# Thu, 27 Jan 2022 23:41:34 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-130e950e6fd637910aab7091bd642e931a601a4cb070782644264ea9b3283031.tar.gz"  && echo "4c580d08afabb56f120f4b3b310f10858508729953a738b0734d857158c63be5  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ab4651db2b38ccb9987dbd8f89afc7b18dba5f4886456b9fe2c3f153e0cb1a17`  
		Last Modified: Thu, 27 Jan 2022 23:42:06 GMT  
		Size: 62.4 MB (62391060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2bcae1c28206ab057633f715df38b6e8f1700cab1e2a8de3bff04229114e69`  
		Last Modified: Thu, 27 Jan 2022 23:42:40 GMT  
		Size: 452.6 MB (452614621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
