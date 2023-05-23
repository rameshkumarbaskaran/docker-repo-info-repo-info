## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:1141ff51486ef628678f1a053bb835ce6ce737940c642b741efb24827afc7d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:0c75637ce9cbddd52606bb612a42fbbec794a0e8ef7e1f761825040af5307542
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50448951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d8d66a47ab8b4b209575b8ea0b0d6d99dfe7390526cca8483e1a47346c2a89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:20:48 GMT
ADD file:d4a7edc71a1c6e3bfb96a96e4afbd73ee33ba722e95bb147a7d006e29d7f1719 in / 
# Tue, 23 May 2023 01:20:49 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:20:52 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fbdff6ab3c866bb827700b7cc9735700c1012f34edcde92ace8b123cca97e9d4`  
		Last Modified: Tue, 23 May 2023 01:25:04 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ed73dccb1aeb8b70e1278c1d0765f5be7b35714a42c96418649f4d73d09f76`  
		Last Modified: Tue, 23 May 2023 01:25:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1179c1e78e5bf235b4d68d7aa1a3776a08b6e1c05c234b3f8f45ed52b58c37d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c418eceed6b6b67322929efdb000a509c0444ac744937de11a48a6a41f2e47fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:58:28 GMT
ADD file:c01c1e55a32cf16d6866f2777cdab993547c9d3146a52e544ca51a9ccc509943 in / 
# Tue, 23 May 2023 00:58:29 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:58:32 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3d19d8a6bda91ea2f74badb378612f4de79d44843359fa77b6729117c91e2909`  
		Last Modified: Tue, 23 May 2023 01:02:41 GMT  
		Size: 45.9 MB (45916514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c978153a76e0579feffa366aeefa92aece7ce510744bb38c66577f6d75b1cde`  
		Last Modified: Tue, 23 May 2023 01:02:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4e0ca308da5db1e24a4049423965b0199fc0781d988a1ca792257f5d140ca7eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49238531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5771dd59823d24df83de6b00702d43f8cfeff9ffbad9e55a49ab06e347e5414b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:34 GMT
ADD file:2b432f06d80368a0aa70a57bcd07324e818b6b65b1336463e006b3cceeec5b02 in / 
# Tue, 23 May 2023 00:43:35 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:43:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:44d886d3df364a0fe6793fd29d8ba173862fda98799b137e777715ec187529dd`  
		Last Modified: Tue, 23 May 2023 00:47:00 GMT  
		Size: 49.2 MB (49238306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a9318c0b6e4f22781a456e41571949f5555b86d27b09b516fe6fe7cb942e74`  
		Last Modified: Tue, 23 May 2023 00:47:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:18dcc41fec8ade13c438d785b2cec1944fac2a2e95d255507d721f59181c6e90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51205887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60a63feab02634dec995df892b89aa5224d36e77449a361c3acf47a355abad1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:40:16 GMT
ADD file:f325a21337c4f12d2e4d33e79575f5def109973d55be6718dd79cd88d2f1fe90 in / 
# Tue, 23 May 2023 00:40:17 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:40:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:61be7484f153c0c17d8706c487d19cc83c629ffd8202911ed497d1b6b6bc7d3d`  
		Last Modified: Tue, 23 May 2023 00:45:33 GMT  
		Size: 51.2 MB (51205663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6378eb9d571d3a8b41ef3fa3e8d27649853fa60b5cf98dea48472a80ec586b61`  
		Last Modified: Tue, 23 May 2023 00:45:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
