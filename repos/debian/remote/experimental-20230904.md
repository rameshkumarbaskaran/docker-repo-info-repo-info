## `debian:experimental-20230904`

```console
$ docker pull debian@sha256:f4fb8ba4af85d9f8f747de0ca96be0cdab59814b6e71a0ec9c29b2427241bcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; ppc64le

### `debian:experimental-20230904` - linux; ppc64le

```console
$ docker pull debian@sha256:4b30d009b07f0bb66aec3a388b4d792e297fce4e3fcdb246538ab41ba6167930
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53430049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3f8143cffd39b692b1b7dbe756b6e8fb57fe74b946c192f7473a5f2eed617d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:28 GMT
ADD file:689b71ce1e06732939c4a9fd605f01bf0c2bb0a103a6e8ad2d628aaf3957202d in / 
# Thu, 07 Sep 2023 00:21:32 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:21:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b7956b481f448c7c033428e86a46af1c78240a8b8bc6d641e8c9770f7a239f27`  
		Last Modified: Thu, 07 Sep 2023 00:28:36 GMT  
		Size: 53.4 MB (53429827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba777a92cf8d88bfef717f2b48875c502bb9d9733bcc55ac9f7536b1a1c90a7`  
		Last Modified: Thu, 07 Sep 2023 00:29:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
