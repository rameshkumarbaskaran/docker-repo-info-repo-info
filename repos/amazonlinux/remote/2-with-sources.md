## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:d644b20bcf5d2b2d8904a9d71eef795f251eb514e97e17a982bd15864042ef9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:914aee596ed80daaab3f5cbc0342b362fc1261b3c4cd92c91f265000276fb43b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.5 MB (492476555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17d3ca95aa8b0c3404dc13254676645e50e7a3f73acb29e6f7c9d0dd37f0ca2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 01:19:49 GMT
ADD file:a69ca7a5499bcd9d6e4317fdbd7256e93be44364bb746f5da10b4268c090bda0 in / 
# Fri, 16 Dec 2022 01:19:50 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 01:20:13 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-52d2c3a868ebf38a0a4b6507974840bf5b25c0df21c9a22b94f87c8adc49de9f.tar.gz"     && echo "0710556cdc469c82ec859b0f7a96ff503ec089745b5f361b9bb32b0adacf0e8b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5b4a36b5b78f93a5f470cf722b313bb32cddb0f8e0fa0db348059b5c0881b04f`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 62.3 MB (62328625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b23b3531e4058e9837a9bbbfdc794d78f6314bc7d1a358ace113a7c07811a8`  
		Last Modified: Fri, 16 Dec 2022 01:22:31 GMT  
		Size: 430.1 MB (430147930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:94ca39a2857f9404153f086e20506a7072cb51b586687e56f31e02eef0857560
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.1 MB (494112129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bc106aaefa1dda62326aa8d751b3878633885a28373561b571dad165df1b4a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 00:41:26 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-52d2c3a868ebf38a0a4b6507974840bf5b25c0df21c9a22b94f87c8adc49de9f.tar.gz"     && echo "0710556cdc469c82ec859b0f7a96ff503ec089745b5f361b9bb32b0adacf0e8b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc3278230a7a767ee02870d022dc903264ac1c0024c37854a942fba7d0fa1ed`  
		Last Modified: Fri, 16 Dec 2022 00:42:45 GMT  
		Size: 430.1 MB (430147915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
