## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:7b2b287d2191d04ecc73d0b6e69ced3c8538008463f7ef351624f3f8922f5dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:eb03889b4ba3cedac439ce0d5c9f27234109f71356684cf4ceccb8d9b245b5a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.8 MB (387784962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20868dc236eb38a2f45fab9b54c56ea5f685204f68019e30fa40d04ec7381912`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Oct 2022 06:50:24 GMT
ADD file:255cfef7726a0d303aef1490fb1cfcf29e287e0d8d240b878de9addd76ae894f in / 
# Wed, 26 Oct 2022 06:50:24 GMT
CMD ["/bin/bash"]
# Wed, 26 Oct 2022 06:50:47 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-14e16a3e28a8c27ff919b56d44ea297047f17e0eeadd435b2d71b68d50102537.tar.gz"     && echo "cee7a872aa60832489fa047b858cac4c9d5076a9a595d514fee06e816d406f80  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:716ba0edb5da96c46c26a53c134cd740ead0345b7360bd6b9b467c7d00c8a677`  
		Last Modified: Sat, 22 Oct 2022 04:05:57 GMT  
		Size: 57.7 MB (57654075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f86aea60721dcdf4beeecb63a8df31330acdac43fe37466a09f951e571d1cee`  
		Last Modified: Wed, 26 Oct 2022 06:51:50 GMT  
		Size: 330.1 MB (330130887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:6b5dade9f05691b289fbbcd0e203d6e44ac7bc4c9a7bd8049e26e13e0a7b57c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.6 MB (385563209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77e861f60a2da3e2c3af5d4dcb8cd19a11a1862fa9b80ddccb0c168e8e3ec9f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Oct 2022 00:39:41 GMT
ADD file:a2aadf3cc267a952a6497ccfe5fd0447ab2279d5a88739bf90af1e60794933ce in / 
# Tue, 18 Oct 2022 00:39:42 GMT
CMD ["/bin/bash"]
# Tue, 18 Oct 2022 00:40:04 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-7d9a61be4e4c4c426d147ee8e001d0fc0ee22e31883c1aa4a6e093a70e79f0a9.tar.gz"     && echo "93f9eb8517f6f82afa0a927f6edf8d11199d40cdf454b8099ef820e79ac7908b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ee9406179427e6b6af08f2294110b752ddd93a1ca950b1572d22e517a92a46a2`  
		Last Modified: Tue, 18 Oct 2022 00:40:45 GMT  
		Size: 56.5 MB (56481754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f3324e83ad5f6d382027fcf8d3c3b31785ddb076e0ccee7669e38742e29ce2`  
		Last Modified: Tue, 18 Oct 2022 00:41:16 GMT  
		Size: 329.1 MB (329081455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
