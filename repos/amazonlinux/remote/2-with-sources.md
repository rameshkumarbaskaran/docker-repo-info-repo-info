## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:a4a7095f6cae0281cf3a5f357eda5174a0e2ee3fb1f584858f2740c0958a7eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:f1c531eaf600c693158c1d1ebbead9146809d78fab280d8bb9fa3b255b8c5af0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.4 MB (486378202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1900d5d0b057d3ad0be96c67ba2666b4016b5a9e87c34e4442e61d12d4002336`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:19:40 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d7c2b2aa50fe3ff7023a3909084d659b7f234ce37cb2b8a54bc449bb682a27`  
		Last Modified: Thu, 22 Sep 2022 19:20:48 GMT  
		Size: 424.1 MB (424074933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:c64709a723326277e8bd139dee26c099248a5cfdc15af39276fdab5bfab370e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (487987310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e561a7921606d2497a6dd0c931d14e2c4efc3c741a9a665cef47c145e63222`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:39:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-e805f912bcb0541240fd70fe7e7f23e3b79a2c5ce3c273054b3efc087e0cc6a1.tar.gz"     && echo "726894e6d2bbc0a7301d9a191b1197b554ad07319a01e726c537d27e73953785  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366907dea1a523b535578b50385542ee460f0d786719b57a5b8a57f84d86c59c`  
		Last Modified: Thu, 22 Sep 2022 19:41:14 GMT  
		Size: 424.1 MB (424074892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
