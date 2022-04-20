## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:3409361409267e7cb8a1dec09b87ae5c7d4e623850ac8fe24bf5fc9df409349c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:b1f28eaf2b0f6e1c4fcb2de8d2e55f1500310cd6f8c702a34add85c9ab3031d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55578956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69efe536855be0685b2bb92a85e7729b27558103d276a9517abee930f368caef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:42:54 GMT
ADD file:b5180fc4d45b984afa69f3cdfa95980bcdfd76d75f704f74f1aa60e416272f1a in / 
# Wed, 20 Apr 2022 04:42:54 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:42:58 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8cb01d170a54a4c7fd7c1969e79df0a453468ebabfe1d860b863f7a3b6fbbc2f`  
		Last Modified: Wed, 20 Apr 2022 04:47:18 GMT  
		Size: 55.6 MB (55578729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02313a896ab9477f41a3f1fdb81b645fc2ff3eeebe183d0249e0f7a7ff945c17`  
		Last Modified: Wed, 20 Apr 2022 04:47:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e2d661d16fe6595df5b419c0dddda22a650cc261a87214f4b9c716065d33b015
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52995752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58f9147e6c6b9c205c65ebf6a1c33c09eae68d777b2b3b5386ae4285c48e09f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:07 GMT
ADD file:6b5b5c095508b777a2c8b2633d97d6143bfab0320bed58e8e335179bfd681fc9 in / 
# Tue, 29 Mar 2022 00:49:08 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:49:19 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9b209f6efb315c2c09d16e50d6077a10a401191c741a83c3c6c0767fe202d69d`  
		Last Modified: Tue, 29 Mar 2022 01:03:30 GMT  
		Size: 53.0 MB (52995524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08fd506ad8b11a6995ff0d3355d95bd68f0132ea316c6325d5f0cec940941ec`  
		Last Modified: Tue, 29 Mar 2022 01:03:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6a5ee7b5b875a2767b92a0abb98f0cc28d5916b46e9bfdc22cebae0b284649c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50610028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac9386130d42b43f0a6aa0ba7b15d2bcefbd0fe80b757b6ffc3311fc5a7da7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:16:59 GMT
ADD file:5ab9a8a4847f677425562eebef8854e58592bb57501d4bc6f521315d90815c3c in / 
# Tue, 29 Mar 2022 02:17:01 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 02:17:13 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c7c8b286eb908a262d0005e4560150fabc15db4a3531f7e00f77b76643457e6c`  
		Last Modified: Tue, 29 Mar 2022 02:32:14 GMT  
		Size: 50.6 MB (50609802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f44aedd4e60510861dcb7935a8a1c48882ad350349c54e886ef5f07f034098d`  
		Last Modified: Tue, 29 Mar 2022 02:32:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a7ce268a65810bc0a624aa6f8c2252b1898767a3b9951cad9258803b3a366919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54493515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac6fdfbac43d0d5177740962c16caac4303ff648ed775e86bd445f839dba1ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:28:29 GMT
ADD file:23397ad30e34521aa2c0881ab09c9c75f58316594a1c14f01cfcb212161c32fc in / 
# Wed, 20 Apr 2022 04:28:30 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:28:36 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c6d996fb7c2fde9d95056213e2cc0a2ea025cc86ce1ceeac46b8c51b2d458d84`  
		Last Modified: Wed, 20 Apr 2022 04:34:39 GMT  
		Size: 54.5 MB (54493289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf32b5d72b6a2412051bc228e2f98ceb6276b3c68dcfaf7b951d518ae387c31`  
		Last Modified: Wed, 20 Apr 2022 04:34:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:ea850cc0c0300e16631a5152a791423326531417f404d2779f4bfef1082c9617
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56628446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fd4f59f10b2528647b2c2ddc0f47516142f5e7f4849a7b2ec757eb418836c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:41:20 GMT
ADD file:828aa883b729cb9e3bbc9efef043626425a2803461bd7b07862d746e2df08c10 in / 
# Tue, 29 Mar 2022 00:41:21 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:41:27 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4e0acfe1e9e31a265994eee72788e1a0b4b33edc5c9d6fc978fd65d87aa94b53`  
		Last Modified: Tue, 29 Mar 2022 00:47:47 GMT  
		Size: 56.6 MB (56628219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd41cbda449a264c8118f874c26f32089f9845fd6868ec89b0875623505026b`  
		Last Modified: Tue, 29 Mar 2022 00:47:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:718685db3cd4f848161727a37e8452a499e8ebb8fdbc4bd98662e8a9085c0f5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54240562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595d136793bb4f998f309a5990bb19fbbd7014f1738ce8775e136c6a0c99c17b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:40:39 GMT
ADD file:88e75745fdbfd0784c1c18134a0a52a5534df18201a6f49555a5c618b4531804 in / 
# Tue, 29 Mar 2022 07:40:44 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:40:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bdc3f4c024aea887030bcf477ee808da6aa3e6683fb111845d94ab4f2480ff24`  
		Last Modified: Tue, 29 Mar 2022 07:50:58 GMT  
		Size: 54.2 MB (54240334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c073b220886baed5bbefb457357d80edad91c1cb4c1f6285abd66f85bcfa6d`  
		Last Modified: Tue, 29 Mar 2022 07:51:08 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d0430aabdd1681c17f7cf96bcb1d27d94a977567d47b31b40b627cf987b6a5e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59999648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db205419660895e5fcc1894bc73068a4671088be6afa3b37a6a447d668bbb336`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:20:10 GMT
ADD file:c9ff325b9fe680d344c36e7e25729f90711bdf646908892ebdc0f3a53d92bc50 in / 
# Tue, 29 Mar 2022 00:20:29 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:21:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fc5522fc3ca5c5e9e4af133a35ed8a4e104c9366b7ab66c3cc5601aef68f175a`  
		Last Modified: Tue, 29 Mar 2022 00:30:15 GMT  
		Size: 60.0 MB (59999423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5116f2188bf2a8e74c4da46e1d7f424271f8c17836b62f3ec039898c7d564`  
		Last Modified: Tue, 29 Mar 2022 00:30:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:8d295f958c6a9539ada7f61e5adf7cca5b51f472624e5bdc3dfa646a06993954
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53839290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b3ba1b73b6da5647126b52dded17237bf57bcf89467e1f475cae21a8460ae4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:05 GMT
ADD file:9a99e896abdfac4163e20511778572abbec89bf317a3c3dad1f6fe0c63b126b1 in / 
# Tue, 29 Mar 2022 00:51:11 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:51:18 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4c231abb22533340c714e28363f98b83f5da88a6702fdfc7d06ed65b8f2e70e1`  
		Last Modified: Tue, 29 Mar 2022 00:57:13 GMT  
		Size: 53.8 MB (53839067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abbe3ac21a3fb5ce958ee5dccbe9a4c48d2c4b7b73fa159cf6f116722e60645`  
		Last Modified: Tue, 29 Mar 2022 00:58:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
