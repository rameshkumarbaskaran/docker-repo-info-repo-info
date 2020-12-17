<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03.0.20201028.0`](#amazonlinux2018030202010280)
-	[`amazonlinux:2018.03.0.20201028.0-with-sources`](#amazonlinux2018030202010280-with-sources)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2.0.20201111.0`](#amazonlinux20202011110)
-	[`amazonlinux:2.0.20201111.0-with-sources`](#amazonlinux20202011110-with-sources)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:c51f954d859ae9e93f5ecbe8a1132659e39523098b98f9563ffd85b7e1c5cb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7d26828be43385154dc3a82a1f99582aab4393627d42c7fd6f30eb6a53ce1756
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62388725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9c4a7803b516986783f06f67b1633a79f722a5f1020e13e45b2b25b8eceb54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:44 GMT
ADD file:57cbe23b8338dfe8556aa5f457a9536aa0e77d85a240a9fdf983475533103983 in / 
# Tue, 30 Jun 2020 20:20:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c9b7c64960cf08ea94a99af6be882845791831279dd11cc6b5e2d822cd07d521`  
		Last Modified: Tue, 30 Jun 2020 20:22:52 GMT  
		Size: 62.4 MB (62388725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:9176d717c354eac59d8663a7e7ad0104c78ae224c39f1348e0b9876b1adaf127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3cf2daadc91456359e4ae9e026c7d4eefe9c8e7de92022934b026e42e53c934b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.2 MB (449205154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bc71b24526296605dbb1eacf91d9fa3044556bff9e493bab7d2fe38fd1c724`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:44 GMT
ADD file:57cbe23b8338dfe8556aa5f457a9536aa0e77d85a240a9fdf983475533103983 in / 
# Tue, 30 Jun 2020 20:20:44 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2020 20:21:04 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-de8e94c334f37301fbb7ac231f1decb67297aa7138fb78c484cf0a2e5f930f11.tar.gz"  && echo "6a4587bb7665170c749dde5bfe60522fec92b691c3e190abd7ac089908fb8ae7  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:c9b7c64960cf08ea94a99af6be882845791831279dd11cc6b5e2d822cd07d521`  
		Last Modified: Tue, 30 Jun 2020 20:22:52 GMT  
		Size: 62.4 MB (62388725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04759c21924907a37db95bd7a1988d1f037bbd8befbc41b5d195d069b993dae0`  
		Last Modified: Tue, 30 Jun 2020 20:23:17 GMT  
		Size: 386.8 MB (386816429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:134313700ae674a8e81a735df31c07760ee4a6afe77a7a951e00bb2bc003b3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:1481659e18042055e174f9f5e61998bf7ab57f8c9432f3c9412a56d116cc0c68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61716540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2cc467a2bce7ffc9e2d6e38a87f6ec89c1c93bc83ff575e8021bb592f9ad2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:45432827a9886949d2a5a97ad4fce1c69bc6078d0627b67e893c71b7f758aad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63675700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484c58753c370914824f30cba19b77f0e3da15d77a636c8cacdb202d23614fad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:c51f954d859ae9e93f5ecbe8a1132659e39523098b98f9563ffd85b7e1c5cb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7d26828be43385154dc3a82a1f99582aab4393627d42c7fd6f30eb6a53ce1756
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62388725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9c4a7803b516986783f06f67b1633a79f722a5f1020e13e45b2b25b8eceb54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:44 GMT
ADD file:57cbe23b8338dfe8556aa5f457a9536aa0e77d85a240a9fdf983475533103983 in / 
# Tue, 30 Jun 2020 20:20:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c9b7c64960cf08ea94a99af6be882845791831279dd11cc6b5e2d822cd07d521`  
		Last Modified: Tue, 30 Jun 2020 20:22:52 GMT  
		Size: 62.4 MB (62388725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20201028.0`

```console
$ docker pull amazonlinux@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `amazonlinux:2018.03.0.20201028.0-with-sources`

```console
$ docker pull amazonlinux@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:9176d717c354eac59d8663a7e7ad0104c78ae224c39f1348e0b9876b1adaf127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:3cf2daadc91456359e4ae9e026c7d4eefe9c8e7de92022934b026e42e53c934b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.2 MB (449205154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bc71b24526296605dbb1eacf91d9fa3044556bff9e493bab7d2fe38fd1c724`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:44 GMT
ADD file:57cbe23b8338dfe8556aa5f457a9536aa0e77d85a240a9fdf983475533103983 in / 
# Tue, 30 Jun 2020 20:20:44 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2020 20:21:04 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-de8e94c334f37301fbb7ac231f1decb67297aa7138fb78c484cf0a2e5f930f11.tar.gz"  && echo "6a4587bb7665170c749dde5bfe60522fec92b691c3e190abd7ac089908fb8ae7  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:c9b7c64960cf08ea94a99af6be882845791831279dd11cc6b5e2d822cd07d521`  
		Last Modified: Tue, 30 Jun 2020 20:22:52 GMT  
		Size: 62.4 MB (62388725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04759c21924907a37db95bd7a1988d1f037bbd8befbc41b5d195d069b993dae0`  
		Last Modified: Tue, 30 Jun 2020 20:23:17 GMT  
		Size: 386.8 MB (386816429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20201111.0`

```console
$ docker pull amazonlinux@sha256:2b5349aaac7dc63708a3a12037dc85664ea5b188b0a55260cb02b220f5196c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20201111.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:45432827a9886949d2a5a97ad4fce1c69bc6078d0627b67e893c71b7f758aad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63675700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484c58753c370914824f30cba19b77f0e3da15d77a636c8cacdb202d23614fad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20201111.0-with-sources`

```console
$ docker pull amazonlinux@sha256:8ab77507ac34372240199b0a8b37c7af223b45655efad1a9d2bd5c927295979b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20201111.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ebc9175447a4e72503cd902746efcf5aa1a98083058ad31402aa8f88a6c7dac7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544486382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a634c2bd30b5b7c23048746867a8df08834724fe73aec1d890f6aa8f9341a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 22:49:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96442617fa0b6c8b89a6c32ec48a25e51e3358effd21430e95799271c016dc4d`  
		Last Modified: Thu, 17 Dec 2020 22:50:31 GMT  
		Size: 480.8 MB (480810682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:d9fff531974bdaebd239cc6eb7f69a78b0413579bfed37d878af3a03682a47bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ce49a5d54788eb0754c038d3fdc1ed815da00be1df787c03cafea1503766fcc1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.8 MB (476804109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fadd5eaa0b1347722638a6d12ce8057456acecc2e2f414e41c886205250c1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 22:20:10 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-4a2709d0b184c9b7a5e4b01c08f0a95ddb949a8af3fb12847920b6fc8cad8033.tar.gz"  && echo "d51679d0ed0ab3b0a8eb3c2a40b03e5c5e6d7b11a13fa6f729b2461204dfb1b0  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77428ba98702146aeb373ef1d9192fe64ca55636a3109ee715326ffdb55e5e5`  
		Last Modified: Fri, 31 Jul 2020 22:21:01 GMT  
		Size: 415.1 MB (415087569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ebc9175447a4e72503cd902746efcf5aa1a98083058ad31402aa8f88a6c7dac7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544486382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a634c2bd30b5b7c23048746867a8df08834724fe73aec1d890f6aa8f9341a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 22:49:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96442617fa0b6c8b89a6c32ec48a25e51e3358effd21430e95799271c016dc4d`  
		Last Modified: Thu, 17 Dec 2020 22:50:31 GMT  
		Size: 480.8 MB (480810682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:134313700ae674a8e81a735df31c07760ee4a6afe77a7a951e00bb2bc003b3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:1481659e18042055e174f9f5e61998bf7ab57f8c9432f3c9412a56d116cc0c68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61716540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2cc467a2bce7ffc9e2d6e38a87f6ec89c1c93bc83ff575e8021bb592f9ad2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:45432827a9886949d2a5a97ad4fce1c69bc6078d0627b67e893c71b7f758aad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63675700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484c58753c370914824f30cba19b77f0e3da15d77a636c8cacdb202d23614fad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:d9fff531974bdaebd239cc6eb7f69a78b0413579bfed37d878af3a03682a47bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:ce49a5d54788eb0754c038d3fdc1ed815da00be1df787c03cafea1503766fcc1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.8 MB (476804109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fadd5eaa0b1347722638a6d12ce8057456acecc2e2f414e41c886205250c1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 22:20:10 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-4a2709d0b184c9b7a5e4b01c08f0a95ddb949a8af3fb12847920b6fc8cad8033.tar.gz"  && echo "d51679d0ed0ab3b0a8eb3c2a40b03e5c5e6d7b11a13fa6f729b2461204dfb1b0  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77428ba98702146aeb373ef1d9192fe64ca55636a3109ee715326ffdb55e5e5`  
		Last Modified: Fri, 31 Jul 2020 22:21:01 GMT  
		Size: 415.1 MB (415087569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:ebc9175447a4e72503cd902746efcf5aa1a98083058ad31402aa8f88a6c7dac7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.5 MB (544486382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a634c2bd30b5b7c23048746867a8df08834724fe73aec1d890f6aa8f9341a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 22:49:09 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-82a79f6229fc0fbe90213d731495bf8a1f3a71fc7d38b3585b8e1210fe79f494.tar.gz"  && echo "1aa350c8aa2873c481ff48ee9cc8754d927da4a89d127bfb0aed9d77fb236a47  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96442617fa0b6c8b89a6c32ec48a25e51e3358effd21430e95799271c016dc4d`  
		Last Modified: Thu, 17 Dec 2020 22:50:31 GMT  
		Size: 480.8 MB (480810682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
