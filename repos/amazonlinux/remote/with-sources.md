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
