## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:c2f0c611f77e8ded995da88754355e30443e07c251f4b30d29bf06a7a1b30d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:c2f6a88e3f9cb6221b13a2d961456a081975b936580387b6933cfff6e664af9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.4 MB (485371765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8932d75666cadda98036af5cd135cad7a648d26fc9b62458558ca3b2a56a435`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Feb 2022 23:40:28 GMT
ADD file:871c80292a1347a65a30c9d2cd343d927528a61b8d89fd82f268d5f8ad4d2944 in / 
# Fri, 04 Feb 2022 23:40:29 GMT
CMD ["/bin/bash"]
# Fri, 04 Feb 2022 23:40:56 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-86059ff059c15219c13900625367028ea52b1d95d6f6515947fe04983baf9add.tar.gz"  && echo "7cbab49134e393024873c4c8ad4937d84c8b7ed316b4d6260ae6b425cdd89e91  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:f964900200fc1f8473ac70d9da14cde8bae251ffb4a8f4792e2bf9baf6aaac70`  
		Last Modified: Thu, 27 Jan 2022 23:12:55 GMT  
		Size: 62.2 MB (62237845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df40d5f106fd4ab71023a3b15de586ad3165bbec356559856b77c24ad4d33883`  
		Last Modified: Fri, 04 Feb 2022 23:42:04 GMT  
		Size: 423.1 MB (423133920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:f58dd8b85d7147b4896f4d240af84876653ff9923fb6cfe0880a74a82297628a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486991491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b947352f3862b8967e6d17d19f985aa482f0f5cb748dd0e5f17e8eba20b60748`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Feb 2022 21:33:28 GMT
ADD file:38bb92c68a8a2ac1145ea8d422911f6f0d9c62cccc02b3bdeda096047efecef5 in / 
# Fri, 04 Feb 2022 21:33:29 GMT
CMD ["/bin/bash"]
# Fri, 04 Feb 2022 21:33:56 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-86059ff059c15219c13900625367028ea52b1d95d6f6515947fe04983baf9add.tar.gz"  && echo "7cbab49134e393024873c4c8ad4937d84c8b7ed316b4d6260ae6b425cdd89e91  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:591d91c97b5df29e14efc53ca38020094df8fa114d32d412bb8f02344aad2411`  
		Last Modified: Fri, 28 Jan 2022 02:04:32 GMT  
		Size: 63.9 MB (63857619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2457150579cd30968d3d34537bde803d2fba631f46f9e31090da275e0b41cb`  
		Last Modified: Fri, 04 Feb 2022 21:35:14 GMT  
		Size: 423.1 MB (423133872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
