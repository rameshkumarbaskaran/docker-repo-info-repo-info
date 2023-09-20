## `debian:buster-backports`

```console
$ docker pull debian@sha256:0294011677c24e779afabaf1d48bb2ea1a8085aec00477484f51271c2aedccd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:7d6cf6e80308f63202661624403f00c90695749b655ba921e65ef03114a57e16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50498386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb828d06d58c2e0155b6cd92611a4240d51c3930e0b6dd1c661ca87f8a22f4e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:13 GMT
ADD file:5a868c8105f7b621ffe46e19453d846faef824601a70979f6ef2bb46076151b5 in / 
# Wed, 20 Sep 2023 04:56:13 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:56:18 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0dfc3f78750b97e03b66f316b37e155e3de173a8ac79942f0511888531fbe5ac`  
		Last Modified: Wed, 20 Sep 2023 05:01:23 GMT  
		Size: 50.5 MB (50498165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722eb998e07f3fb72145a706b643aade819dc34b9e7b98e37b4eb6554def739b`  
		Last Modified: Wed, 20 Sep 2023 05:01:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:722fc65964e18a5c128644a8ee0a7050326594890f6f75f748d3f2e9a2fe6277
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c230c9f8877a53e3bcd4f708375ef309e18abb1fa9f14e5c19847624b66b5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:44 GMT
ADD file:61a164f3dead6329acddcce40680f06b7b0f27e5620a1afd975e186153e42077 in / 
# Wed, 20 Sep 2023 04:57:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:57:47 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6e2ab1511f035b8d0208496939ad6f66778c120d1c102125b629bdb138ce4a14`  
		Last Modified: Wed, 20 Sep 2023 05:02:14 GMT  
		Size: 46.0 MB (45966225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf08472c19eae8ca84257f25cf4e03b364a844c61e145d1ff3348c3148259441`  
		Last Modified: Wed, 20 Sep 2023 05:02:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:40564b071a06cf92cfc75676968cccb93712c96637129df5ac69cc72e9801ce2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea13722262708c2a01ecbb48806d3c93d50475bbadf90ac8d7274bddf92cfb68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:34 GMT
ADD file:3ec160f0e210563bfac108f23e5034dda5bc7b513b824ee276e4fc6daf80c89e in / 
# Wed, 20 Sep 2023 02:44:35 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:44:38 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:acd8b5ac4bd39653c2ebe6bd243f4ad2ee504ec9f8feeda9ef727446baf30721`  
		Last Modified: Wed, 20 Sep 2023 02:48:30 GMT  
		Size: 49.3 MB (49290887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca7b9c16ebea7f5028919e69d1d425c3882d50736daba1bfc0ae33fca3242d7`  
		Last Modified: Wed, 20 Sep 2023 02:48:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:4da13c493b7a496aff0a087ca00773b400f6612f89f3079995ea39662422ca61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fad0b1a8cf28c31d6dfea6195f984851d9e8dce35888473bdae4c0cf1ed02d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:42:29 GMT
ADD file:6603eb215d695ca693056401592eb42db80ae6d6fcd314b50322ceb7858c1f2c in / 
# Wed, 20 Sep 2023 00:42:30 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:42:33 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6be8533983dbe30a84ca98eed25142115c1c6e36639d1e5086fd77e3332abc10`  
		Last Modified: Wed, 20 Sep 2023 00:47:58 GMT  
		Size: 51.3 MB (51255415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82eef73bf40b7aa6cd3e0c9d15e8f94cc4a8c5a1919f426ae164ee9dc891d94b`  
		Last Modified: Wed, 20 Sep 2023 00:48:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
