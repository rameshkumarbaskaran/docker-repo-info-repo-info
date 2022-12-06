## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:049de51cdc927242429ed0222f457cba04ed6c40fc68f79f3f0451c13cde266e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:31198c157d684bf44902e7939ab721d7ec4bb55b1b2da46059b18fea942abf2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50449089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631169cb4be41f9c180b2135d3782a706b9c40b8dfedc23ad93ee320ee20acf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:29 GMT
ADD file:143a8fb5d26bb1dc1d9305c7679bc6879e1ad56bf196fef3e468ca805b31c0e9 in / 
# Tue, 06 Dec 2022 01:21:29 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:21:33 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:63afce2ffd8caa6f320f8c2de4348ad65afc9b90c2e9bde7e7ef627f33f2a6cc`  
		Last Modified: Tue, 06 Dec 2022 01:26:10 GMT  
		Size: 50.4 MB (50448865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469693b42bff517e053bb531f378dee93ec4e9a3027123632b1839505ded64c0`  
		Last Modified: Tue, 06 Dec 2022 01:26:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:413fbc091720a8bb3a3a8c3266756470e993f4eacdd8c5860c33968d434abc87
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40b62f7f83a156426fba5d4e8965e1c2348a9f376726034efca40834960bdcb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:59:42 GMT
ADD file:8fd8cda825c15d02c34973f7dfe0bafbea6ef65a0da663aca1b55045c69ccec2 in / 
# Tue, 06 Dec 2022 00:59:44 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 00:59:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fd8e272c3a0dda2db4eee10dc4e8689e197689318a4b437c03fa2bd86320c10a`  
		Last Modified: Tue, 06 Dec 2022 01:07:20 GMT  
		Size: 45.9 MB (45915477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cba2b746456dfbfbecc63c475978134a4a5bb9705630eeac2712ce9c8387c0`  
		Last Modified: Tue, 06 Dec 2022 01:07:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a351d47332030d49527e8170983affe37c35d425e8af861c80323968cabe9bb1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49234009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeca687c40bbbfee9d7b13a258b895ac1bace795451bf8b5164f69bc94a638c6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:40 GMT
ADD file:d3e305927856691817f0b321e3ca76a6ddbdd557f62aa4e25e2501b5c4aae4d2 in / 
# Tue, 15 Nov 2022 01:41:41 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9aca4dab0ca9af54fb0bc3c53006adc1874be641f15371a314b9643b230a590e`  
		Last Modified: Tue, 15 Nov 2022 01:45:30 GMT  
		Size: 49.2 MB (49233786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106419bd0732254a61c54c6eff9ef3004e8f1f13dbfdc2cf6f7b411254998bd`  
		Last Modified: Tue, 15 Nov 2022 01:45:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:09be35b01c99441cfbd29dfcbafb8a8926b6a1512318dad5d45da9606cf61aa4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac201fd4e11ef094042d56e75957ed5e7a0758865ed41a1f8459b99bed26cc7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:05 GMT
ADD file:a38f163ea2aa00d0da6d41e110886005a371094cb39fda5e247f506153001319 in / 
# Tue, 15 Nov 2022 01:42:06 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:42:12 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f617ec91bcf39f4f673f082643fb6396395615449fd76a6a24183c93350e610f`  
		Last Modified: Tue, 15 Nov 2022 01:48:13 GMT  
		Size: 51.2 MB (51207659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614e41d38cbde638aed57b5183515cf7283c2ee42066945d996186323fcab649`  
		Last Modified: Tue, 15 Nov 2022 01:48:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
