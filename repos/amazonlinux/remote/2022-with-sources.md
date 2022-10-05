## `amazonlinux:2022-with-sources`

```console
$ docker pull amazonlinux@sha256:5e477e5056e1f2d8396eca71c9935714fdd31a3f7ffbc67edecbec16230dfd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:77dd340fdf55b940cdc52d4b060c93adcbe7e05cc3e12a09019130c7401d7931
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.2 MB (391152213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aa2c8214c206b8a8e0a99b00da665da27d4cb6bb77ce01dce4765330f6ef82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:19:43 GMT
ADD file:53e1223ac2577a9120a1b918a6969a2f229da88a56ceca0716f26803bee1c276 in / 
# Tue, 04 Oct 2022 23:19:44 GMT
CMD ["/bin/bash"]
# Tue, 04 Oct 2022 23:19:59 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6db34f8cd5e21ad325845bbb40ba13ccd8a11d5f5ec64b74a53c4aabf5f4e82f.tar.gz"     && echo "ca8334aff5f0c8482d413409e35119c142d9208702a27bbba92c69a5f38f598f  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:a8064ab546d10ece855ef4e617864c1d385e149fff22821e280700a12e22a2a6`  
		Last Modified: Tue, 04 Oct 2022 23:20:36 GMT  
		Size: 57.9 MB (57897158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544896198d372500cc3a12d5d6b9faac3193dafb226e54cffd9593e18e8f59e4`  
		Last Modified: Tue, 04 Oct 2022 23:21:00 GMT  
		Size: 333.3 MB (333255055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:d189da355fa602d9b49f2579df6d35f38593ee96973f9659ed162f21955910dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 MB (389950161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d5cc125d8b47dedd0059002952186a317b7ab8675fd82a9c90b8c488065822`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:3f0f875a288565f921dcdd4a86c780ed67ab0c18681ab1b97a7d646867e32c60 in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["/bin/bash"]
# Tue, 04 Oct 2022 23:39:57 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-6db34f8cd5e21ad325845bbb40ba13ccd8a11d5f5ec64b74a53c4aabf5f4e82f.tar.gz"     && echo "ca8334aff5f0c8482d413409e35119c142d9208702a27bbba92c69a5f38f598f  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f1e20b0535c285d016cc63a5a609b903e411c78071837e64ea3314a22ee2f50d`  
		Last Modified: Tue, 04 Oct 2022 23:40:39 GMT  
		Size: 56.7 MB (56695136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00725a1a157c2e1b2b4928f94f0c78fb36b2283c6058a616036be3067167abba`  
		Last Modified: Tue, 04 Oct 2022 23:41:09 GMT  
		Size: 333.3 MB (333255025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
