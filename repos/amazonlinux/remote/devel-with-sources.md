## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:64a7fdc5af1fd9b724c7b28630a2aad58f82d08a3651eace866d061ed3781566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:698032efb39ccbab8dc9abc5dc3b57682f1da1b89aa8a60bed1e5fd24f87e7d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.3 MB (489262019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bacdbeb608c26f31936f6982745dade2ec6c8d386926a8d490da20af6de4a85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 May 2022 23:19:33 GMT
ADD file:8938ca932860236a5478568502c523de28f6fdb1844554dff09a9073e58e2d64 in / 
# Mon, 02 May 2022 23:19:34 GMT
CMD ["/bin/bash"]
# Mon, 02 May 2022 23:19:54 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-30a96c4f6cb306f42c34e07a80efcfbe6980633a9ac34327014a87423221b673.tar.gz"  && echo "eb2de792ff0fb280db260db9b6f4c55b40e52059337fc4c1a293f79f2b4e45bf  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ea1ba8a91f0904c1d69fc8987dcf4d80e75a6f574e1b4a292e9be3e1b78f1def`  
		Last Modified: Mon, 02 May 2022 09:17:35 GMT  
		Size: 70.6 MB (70553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39db4bfd73372833edec2c995c10e909ff279746b73b39bbb9a78a95ef9464a`  
		Last Modified: Mon, 02 May 2022 23:21:01 GMT  
		Size: 418.7 MB (418708131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ac9154ace84c95d05b14c2d4bfea4e43954b6e5f4d24a53ad86005883f8e68ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.8 MB (487811892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa0263e0ffa55f3b9062b5c556fc0f0e1869d31fcf2250385c602a8c083c1ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 May 2022 23:41:36 GMT
ADD file:a7db6c0fde802c761f92fffcc7031a46d1d22f6bd270cfaf0f657e3f6ed18a98 in / 
# Mon, 02 May 2022 23:41:38 GMT
CMD ["/bin/bash"]
# Mon, 02 May 2022 23:41:57 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-30a96c4f6cb306f42c34e07a80efcfbe6980633a9ac34327014a87423221b673.tar.gz"  && echo "eb2de792ff0fb280db260db9b6f4c55b40e52059337fc4c1a293f79f2b4e45bf  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:81baea72d1f94ce2611f8412d29ad6a68396cb5f45c7e2fe8f0dd9f3bb270744`  
		Last Modified: Mon, 02 May 2022 23:42:40 GMT  
		Size: 69.1 MB (69103820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee46a4843a1e40c260139a6926e48843ee1dc8fa172bb261e89f1ad679162268`  
		Last Modified: Mon, 02 May 2022 23:43:15 GMT  
		Size: 418.7 MB (418708072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
