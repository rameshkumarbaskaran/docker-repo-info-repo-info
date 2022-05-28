## `debian:experimental-20220527`

```console
$ docker pull debian@sha256:fafb1ca92a4043d81af32d857fe75dc3a798b1eae807079a63d9d3eb55718658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `debian:experimental-20220527` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6a80a32d1b374717811012a410dfc52e619238796c8eed8116f33258e7c1942d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52261470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6de65e52754902f3581327bd312a08b529c22b64919cee988055cdb4a17a88`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:43:35 GMT
ADD file:2872959d1380a162e11a052911482db0c296636653647605fb8b01d15b6b84c4 in / 
# Sat, 28 May 2022 00:43:36 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:43:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:586b8a60c851194f5e17a9f5238244c2c05921eba7aa586e6c5c0751b9eb1313`  
		Last Modified: Sat, 28 May 2022 00:52:52 GMT  
		Size: 52.3 MB (52261249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ad4e25696e72a1d8837a91dbffa0c00af68f2b910b61506a6a361dd85b28f0`  
		Last Modified: Sat, 28 May 2022 00:53:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220527` - linux; 386

```console
$ docker pull debian@sha256:d857809421963c75bac0df791a24fc502a9aca4db33b6fc2f50d8e05c532b0e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54158934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83e5df1e94de4d15d6c0348d65f723a7987fe3b10b9ea2a07167642bf5a42b8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:42:43 GMT
ADD file:ddbbafd9c13cb3214a5f4ac7696a1e2849d91ecdb8c1b7c67e6adf47f5b19dcf in / 
# Sat, 28 May 2022 00:42:44 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:42:59 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:45eb7531e9b10f431a1c01cc0540d78d698cf327a45b3c871e3d2cfda8cf77d8`  
		Last Modified: Sat, 28 May 2022 00:52:08 GMT  
		Size: 54.2 MB (54158713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2389f7326fa2ce9a33fbb150ee45d7cfcb4e82c07b7d8e164ea9715bf9158`  
		Last Modified: Sat, 28 May 2022 00:52:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220527` - linux; s390x

```console
$ docker pull debian@sha256:90add0686b81682f4afa2adad119afbeaea8dee4f6f73ef6c6d44091264a430d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51703461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacac0f07bd4e56d2687ca7ceedd966f6d54cad580588b1c1fb018fbec07d532`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:46:25 GMT
ADD file:ca2f9e70e62257fbacb0eb455cee1752c9404754ca7f5149c70058259220b8fd in / 
# Sat, 28 May 2022 00:46:28 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:46:49 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9fb199d2a2726467db59cf4e8de4009b204a5bc0adf9d148f49c09fd9a992e28`  
		Last Modified: Sat, 28 May 2022 00:52:19 GMT  
		Size: 51.7 MB (51703240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8e8f2b28b94c6e77dd3c005049957ac0cb79b7127f87f3fceea85f39a22ddf`  
		Last Modified: Sat, 28 May 2022 00:52:37 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
