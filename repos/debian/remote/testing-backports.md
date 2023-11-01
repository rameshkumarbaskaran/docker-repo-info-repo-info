## `debian:testing-backports`

```console
$ docker pull debian@sha256:6fa8c8d66f66bcb6d7cc7fe2302a83fc993413fe179c4829e1533227f0be3430
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:185402e6da497018ccbdcf6678a7f4aaa7c8878a8e273657278fce1dc559e4cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49487130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3793859ed7a6ca08fde8b3a74600e015bef8279694350928e5340f28c6003c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:23:10 GMT
ADD file:490136e40a0d35b152441fda2b93822007355ecd4d486c38c8155e8b91bd5184 in / 
# Wed, 01 Nov 2023 00:23:10 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:23:14 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cc0e49fb24dacf25e2f403d80c5af0757c0d2ac2e78f76919d7076074002f56b`  
		Last Modified: Wed, 01 Nov 2023 00:29:34 GMT  
		Size: 49.5 MB (49486907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b6c823cd57d1682535defc9208592d2d72c317a7ba01b8f5cbd772730e6bbf`  
		Last Modified: Wed, 01 Nov 2023 00:29:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:957e03ae1d71bcccc77a26585f0352726c1542c08b470e40e27c4fe74e5db93f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47142359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efa520f871f3a69c82c039b14867a6789ffc7d6eea98e80898244c590d0dfb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:49:39 GMT
ADD file:f71f449e36b1e71b504adabf652b4702c420a8fe00168640ab3a28bc80d99661 in / 
# Wed, 01 Nov 2023 00:49:40 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:49:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dd4ad4715d8120d73b710c090035211ea0a6e4bdc9523d0529aaa1d58cbfdcf8`  
		Last Modified: Wed, 01 Nov 2023 00:54:13 GMT  
		Size: 47.1 MB (47142136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730943cca722e286686e0aa75d46f0552dff3a62bc5b2b6a70ec4a4d8985da4b`  
		Last Modified: Wed, 01 Nov 2023 00:54:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0055143d826ea3b9ebba6ed5ab8be3ef31db3d0dfa9f21006907e3aee528f64c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44936411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a669f494cd3d4d58455ef7cba9a9487a6617795b2964c3d6bb587ea4adca02e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:59:49 GMT
ADD file:4516f2a93fa3310ff737ec82b9cc971c88f4ab93f9816544684747da8d5b5115 in / 
# Wed, 01 Nov 2023 00:59:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:59:52 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9c9dc49cc71e601bff4e2e5ac89d218f75d6a313098a6328fede87f7fead5606`  
		Last Modified: Wed, 01 Nov 2023 01:06:23 GMT  
		Size: 44.9 MB (44936188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773ad2da0071deb347e445ece5879ea7c28811ba9372dfcb6182b7b1f745d592`  
		Last Modified: Wed, 01 Nov 2023 01:06:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7f54d7842440ab6402df801cae09a8d78d1b4abacfcbcb4c0d77bba4178c5e53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49495456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2b3b8ed3ea2f6758975a149d7db964e01f3ed4611879ef20d0b6b1c2c90d0c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:41:12 GMT
ADD file:422607799f7f9a353c26d961c9d74341ac8915480afc1832e0a10b1e0bae871e in / 
# Wed, 01 Nov 2023 00:41:13 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:41:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e920ac680f72fa3419c6aa8862ff3df12d1f7f9eea6e98da5486f89f1e356e27`  
		Last Modified: Wed, 01 Nov 2023 00:46:43 GMT  
		Size: 49.5 MB (49495234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006a8f49dbfa5f946e20b40176e4665edbd6d10333ddc18561f16694f0566450`  
		Last Modified: Wed, 01 Nov 2023 00:46:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:c64b7550fe535445c12bb2feb1fd5376a582565ec299f7981b36879d0a145cbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50466614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df703dc522e7a831cf5230355c0083d94fdd76f05f0ea987e3ef314f046f025`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:41:11 GMT
ADD file:c160244e4ed71ec61b98ea044f1432f4281a6d811c799638754294064f8a5354 in / 
# Wed, 01 Nov 2023 00:41:11 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:41:14 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b585f0c376d31a217aae96533ede7c9f4d2738471daf1a9645fa5ec3d36c8dd8`  
		Last Modified: Wed, 01 Nov 2023 00:47:55 GMT  
		Size: 50.5 MB (50466389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fef34b8f68ccd5c669d82882202523efacd46453a1eadff0dff7efd190c2772`  
		Last Modified: Wed, 01 Nov 2023 00:48:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:f174e3024f3edb009dc1dc6954fc2cb2b2f4a9721c5be16313e8935536a9cb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49278856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2b48550b912e982c4e1f1ceb09aab4d312e0ae266966d0f9500ff5f8bdb686`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 01:14:27 GMT
ADD file:161ba149e2f34216d699624f938455bfce0e2b17b5002ff0c1a5cec245e71664 in / 
# Wed, 01 Nov 2023 01:14:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:14:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:57fdaa3381ba73101b85c3a6d4ee561007ebb32dfe69262b7681e433b4ca1d4c`  
		Last Modified: Wed, 01 Nov 2023 01:25:31 GMT  
		Size: 49.3 MB (49278629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad506dfc9317b1f2880300398aee93587b853c9c230f138ef6f76e62d0926789`  
		Last Modified: Wed, 01 Nov 2023 01:25:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:08ac04078af6d7dbed54af216699015b2501a0dc65c1bb3608f52139ab342ad8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53390935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd7490f7df222dacccd320949d2eeaa6ca922536f792150620017ba8f5e8eff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:23:36 GMT
ADD file:2a57f528bf7c5e3f557f80c7b960cad458b8d6815a64f2364bb079efad5cc0df in / 
# Wed, 01 Nov 2023 00:23:40 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:23:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c86f9849ab446c023b055adf524217a29db6df1063fa124656a744d8c5454154`  
		Last Modified: Wed, 01 Nov 2023 00:29:10 GMT  
		Size: 53.4 MB (53390711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4fbd96642acaa7adea3b1c0785d450b903481b0ab956f3d8f7b8783f14a35a`  
		Last Modified: Wed, 01 Nov 2023 00:29:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:0bf928023b87d59726ee83f2d6f84cdff0a474f2c039b046c7891d4b2725d491
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48900402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b8bc93a896dc4da2d384eea204972417ac9681ff6cc58534c1006a4d1866ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:45:04 GMT
ADD file:c1e9cc0f1e50baa8f4578d6066a853f19ddeadaa04b24e2c8666570b775be9af in / 
# Wed, 01 Nov 2023 00:45:08 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:45:14 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:01519b303830161a8a78b116a589cddd3dd917366a480e71bfd6b19f14adcfc2`  
		Last Modified: Wed, 01 Nov 2023 00:50:14 GMT  
		Size: 48.9 MB (48900179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32c93441e178482b49132b308dc844c59a7d8750d2de7829ea14785f49ed87a`  
		Last Modified: Wed, 01 Nov 2023 00:50:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
