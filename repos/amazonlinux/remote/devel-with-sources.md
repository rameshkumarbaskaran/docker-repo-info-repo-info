## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:760d81932d5706133e31f2f83456e19dcd43c0ec0023c6fbb9f41a4c370258ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:fa8b758e194c757f8da89ab20ca1bd5e9453e192a8c2052d719898dd8417c45e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392627347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef88d77fa23bb2a8b1cdffc716fe8eed289a8eef455f685579294f76c85f783`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 00:07:30 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224af1760478d3b5043995f3d5520957bbb16e82027bbe9e0378b6f5c95194a5`  
		Last Modified: Thu, 25 Aug 2022 00:08:30 GMT  
		Size: 334.8 MB (334783319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6d34d82cfc93e13ff3092c803ec471c6df2189ac77c7def89340908e180a717d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 MB (391435816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89db54d4aae5846c92569752a868b2de5ebece60aa6b29d9bcb6a45dd704ed1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 02:31:33 GMT
ADD file:55877c288cf7f8ab91c5637c6aff57101bef1c014d582a662f34b5d2ecc847e3 in / 
# Thu, 25 Aug 2022 02:31:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 02:31:55 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5e635f8132bd60336ba3b1b0b8d4cf0a20780e73e4ed03f6b40e82e16935e74`  
		Last Modified: Sun, 21 Aug 2022 18:40:21 GMT  
		Size: 56.7 MB (56652515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8d0bd20a60b455dd23e6d5a415477a24bc08ceed6abb15fc56778a27f1aa45`  
		Last Modified: Thu, 25 Aug 2022 02:33:11 GMT  
		Size: 334.8 MB (334783301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
