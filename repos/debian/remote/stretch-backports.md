## `debian:stretch-backports`

```console
$ docker pull debian@sha256:b16d0a47bc4d61a0e0a2cfaedff807b9cc4bda4ea19a342edb6b87463b57928d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:f195afeb32f7e2be2633695806db4d48fb7d5a6cc634ba229c4fd00c3d3c108a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b5ab4fe2073653c83f676c23d90d388abd063024f5b9d3fd56e289b436cfba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:23:38 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d917923759143f553c3611ff95ba5147d23e392b7f4f5a4ec655ed008dc0e668`  
		Last Modified: Sat, 28 Dec 2019 04:28:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e5a27b8cc19331a86abf9b9d757209c22717adc56db7b54ada46782d74cca434
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44073248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d755a9a799f9735d1533e36d065d104c55ea66d276c104e57cae0911ef8fa75`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:52:56 GMT
ADD file:003f4ef6ab6701f1cce91c9774e3c1d199cf937ba1641ab43af5ba549c235c21 in / 
# Sat, 28 Dec 2019 04:52:58 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:53:06 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e58f920d198d7f6350a4f92bed980e92dd883ddad00ee7e4667d621ad90766eb`  
		Last Modified: Sat, 28 Dec 2019 05:00:03 GMT  
		Size: 44.1 MB (44073023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a25ca79b0556979d3307911aebfd004e4b8c01d0c49405b3107fce0a049529`  
		Last Modified: Sat, 28 Dec 2019 05:00:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5770286790626f980fcd1f465d3a5ae364d4ea4d2cc234f75aa6ecb54e729f86
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42108349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9444918a496612f4b29be15abc2710293411a62b8951ae81dcd3186046e3dc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:03:37 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8163e95f5def3959961ebe1938a9cff1582707ef2634ce8a8e012ee7d7d4b16`  
		Last Modified: Sat, 28 Dec 2019 05:11:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f9c75220baf69ca4cf231694a09dce49c38d1b3246c288c6103c643e914500b2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43166701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d91ec77c7510aae41f9c013893c47e308894560fe7c828c228c906e2300fea`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:43:24 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c020a779916513720e0d2922a13ea0e629a15bd227a035776f2423ca485a054`  
		Last Modified: Sat, 28 Dec 2019 04:49:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:5341b562efe75bec7bbd97a5b9603c6d9674c9b5e6bb9f123e6c160d43dd77d3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46100318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12aa801e43b8d44f6606bd91b561cb2237150bf29ea6560c24f2ea2f7971c681`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:51 GMT
ADD file:f348ed8c5f7efee9f7e88d9a9bd1d57bca1bf445d486996cb6168da85c0bd43b in / 
# Sat, 28 Dec 2019 04:41:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:41:56 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:410821d7ff8b427b8dfb93dcf31b1836a617f5c09be71f83a16ef2c5946ee700`  
		Last Modified: Sat, 28 Dec 2019 04:47:20 GMT  
		Size: 46.1 MB (46100094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfb2a78da7d8fc4f92b0062f58b041b5afd826669cd7de26c89b301ee8a946d`  
		Last Modified: Sat, 28 Dec 2019 04:47:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:80b30fa85b6f7b90ad44a8446a6c92b45695f420a1933b4b501954341fd16f72
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45652701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61afc2125c3da47920960b62bb02264ade4d8121fa72e927b0948b9422f306e2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:22:59 GMT
ADD file:0da9c5c67cad579be1a33f0f66df515de7f3ad992050c39cbaac281a01be41b3 in / 
# Sat, 28 Dec 2019 04:23:02 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:23:12 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:32185d9fc6268c6a6d87060ea324482fa22129c0f06d0f35e1376ca27b5399a0`  
		Last Modified: Sat, 28 Dec 2019 04:32:44 GMT  
		Size: 45.7 MB (45652475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6968be9df7394df732f7852fd75c85b733bb6c767e481f03205176e69da5dd04`  
		Last Modified: Sat, 28 Dec 2019 04:33:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; s390x

```console
$ docker pull debian@sha256:9b0cc5f6be55bfe5559e96411cf0d81a736d7615c71fa8d912a3dd1384264c1b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45241867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d53b9e9ca898bbde13a6a6d52a5006a1876400968581e0c3845f489eb3dec3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:08 GMT
ADD file:b85ece7344f0ad0749b115e76a51a3b9f322e23bcc8c692cd2edff403ba8840e in / 
# Sat, 28 Dec 2019 04:43:08 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:43:14 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5bf261872a9b22035011c2bf77259c73389d0d5786e4b43bee1df89b5dfada2f`  
		Last Modified: Sat, 28 Dec 2019 04:46:24 GMT  
		Size: 45.2 MB (45241644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993ecc48d1ab6e447038a8659b2aa10105c287c3adee7315c88cdb08914c7ed0`  
		Last Modified: Sat, 28 Dec 2019 04:46:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
