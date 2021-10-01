## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:dacf379827e76019455bb17c1ae75a4a0aab7a4979ee41a81f93fe2e44e13021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:166a07247bb683593f03a556aa010d3bc7273439f038eccee9b5cc0c48af3e17
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.0 MB (543000923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f894820418645903e9eaf82e16f79a3234546d6984b9778f7a495e4373787ef0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 01 Oct 2021 21:20:20 GMT
ADD file:21dc1ad70daefae1cf0e1b3e78fab06decda5cb9bc958d8a178adb3eddd1fb32 in / 
# Fri, 01 Oct 2021 21:20:20 GMT
CMD ["/bin/bash"]
# Fri, 01 Oct 2021 21:20:55 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-9e2410667f949f30b61e785e22df92d79408ac9eca07635984070dda5b1f62b5.tar.gz"  && echo "38104879f82d48a1d2a52ceb37ad6275a2b26ab7596440d3ace779cc54d440fa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:0728ce74490afacced1ac863ee989913071f97c52ab996e46cdd6b5369a2d63a`  
		Last Modified: Fri, 01 Oct 2021 10:54:14 GMT  
		Size: 62.0 MB (61952638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310d2444e47af71010180a773ce686cc6dd57bc3285799bd0d06dbc6d567f827`  
		Last Modified: Fri, 01 Oct 2021 21:22:42 GMT  
		Size: 481.0 MB (481048285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:632af4be148831edf819c225d01bc972d720025c8abe1f380ed88b7ed558b08a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.6 MB (544630263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4f4a131ae28f50b0bf011d97b1b53696821ffb4c50a5b34646890f07b7e512`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 01 Oct 2021 21:39:54 GMT
ADD file:1d2ae2bfc4c1f83dc53f48b42503812d345622ab95d8fc84536216ef3d53d807 in / 
# Fri, 01 Oct 2021 21:39:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Oct 2021 21:40:24 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-9e2410667f949f30b61e785e22df92d79408ac9eca07635984070dda5b1f62b5.tar.gz"  && echo "38104879f82d48a1d2a52ceb37ad6275a2b26ab7596440d3ace779cc54d440fa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5aa4871be3ec1bcadf7a5257231adc7740edac9a612749884f03ab14b4b2d4ec`  
		Last Modified: Fri, 01 Oct 2021 16:32:04 GMT  
		Size: 63.6 MB (63581978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c908c980ccb8ba7613df248e792c1a2fc8eb573c9b00259d9f17810411b39631`  
		Last Modified: Fri, 01 Oct 2021 21:41:35 GMT  
		Size: 481.0 MB (481048285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
