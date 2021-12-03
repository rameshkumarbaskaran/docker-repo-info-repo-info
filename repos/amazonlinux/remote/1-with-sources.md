## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:d4d921a4a191944d7e028f22efa418f978ae39d9b6d451b6d19f8fc1cdbaeab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:da16df68ae7f6ce6fad4123e255ba51d0917030f796e1ef4086a3deaf51e8101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515029612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa111552ce92b077f0e226fd14d250252ec4643eead06a1010743c65016ee472`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 23:20:40 GMT
ADD file:b40f5b5df3c73d89ec477953753f29f16b9ebd38006d73c41b1468302e274d6f in / 
# Thu, 02 Dec 2021 23:20:40 GMT
CMD ["/bin/bash"]
# Thu, 02 Dec 2021 23:21:04 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-d9420f93e86b4ae7e03c24f0e4f98c3c9ea9a63b39646e47c86b1dbadc8bdec5.tar.gz"  && echo "c30aa8fe6299b9787f1287c9b7508bad1f31a056d26cf106d87670b6fe99c16f  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6ce5a5560ab28234e783487f84e4b59ecf9cdd051947c044d6b557746ded7630`  
		Last Modified: Thu, 02 Dec 2021 23:22:29 GMT  
		Size: 62.4 MB (62408287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309de403a6353bf47267c55cbbfd3ce20772653b054e31dd83b30bc40380451e`  
		Last Modified: Thu, 02 Dec 2021 23:22:59 GMT  
		Size: 452.6 MB (452621325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
