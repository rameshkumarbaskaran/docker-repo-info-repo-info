## `debian:experimental-20230502`

```console
$ docker pull debian@sha256:ee545488a4f6ffe0fd5753dc6228f964a6cd200a9bcf7ac04c1d9ae7c43b2c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v5

### `debian:experimental-20230502` - linux; arm variant v5

```console
$ docker pull debian@sha256:3ec7e8d03d0b24136e45f16749d8e235bf15a53f31933b235167d4a787b5c68f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47167286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97b434224c2e1b20ddc7accaa6b3353325c2f0a71b144f0b8014381fe091ee1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:49:42 GMT
ADD file:740dbf70289faed5b254bb33009aaddef87ef73abcfdc2441b61e0be62ac6d62 in / 
# Tue, 02 May 2023 22:49:42 GMT
CMD ["bash"]
# Tue, 02 May 2023 22:49:50 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c7b5fff53169be147228f50722828c1946b9253a79b37d14d755411593e715be`  
		Last Modified: Tue, 02 May 2023 22:53:28 GMT  
		Size: 47.2 MB (47167066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eade863a9332ac1f6ffe4dbd68aaf23ffd777b9c81619aeeccc0bf1aa40899e`  
		Last Modified: Tue, 02 May 2023 22:53:49 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
