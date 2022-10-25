## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:da7e4b12b872abffaca011ab06f1304e706b4cc74c1b26bbcbe7e05585732e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:cc966d558163b2c444e75b9f98f82b9ff3937ebb3197e77783e9e929bc373136
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50447986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524292ee0b4e17fa1f18838b052d0c780295ce929da220ec105ceda9703913b2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:21 GMT
ADD file:326adf2063d8d292211a8c3f1b0ed03faeac6ac47a2bf31c02c22df04e81a3eb in / 
# Tue, 25 Oct 2022 01:44:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:44:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5c3cab76daeb46f383600922bdc00d7e2095afa471338147c1901af943ba4792`  
		Last Modified: Tue, 25 Oct 2022 01:49:00 GMT  
		Size: 50.4 MB (50447761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888e60dc9add3193c2ae715a89e232822346e2a800d7cd75e237f4fc26fe4bbd`  
		Last Modified: Tue, 25 Oct 2022 01:49:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:05ecd52738c6b9dd9c8360511c0266b2f9ed5fc4b17af20843c98b8628a22640
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c823d472049dfc91e28ec77cc3ac0c4c55d6a5be8ed4713fb2dde83abbd697d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:12 GMT
ADD file:c4b78f22401af0cad6ac70191492b42eb3613516a46b123ec64b9ab0c81b4ee5 in / 
# Tue, 25 Oct 2022 03:15:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:15:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:facb5eefe2e92765f79b56f7e31fbb17246a13cbe4916b33b6774f27283c88f0`  
		Last Modified: Tue, 25 Oct 2022 03:22:38 GMT  
		Size: 45.9 MB (45916221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04640bc18d5d0c26cd11a3732560cc0777ba902b5c9753925c970590b772b4ce`  
		Last Modified: Tue, 25 Oct 2022 03:22:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ac8fa46e9ac5d85d16b8e1a78456cefebb9944b4f519ca3e0121915f62faef63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49229088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76127c128d286fc847d4c4c0a832081440dc74c78b412d1ff3e9517fa90e7492`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:22 GMT
ADD file:b52dee81f9bddca289cf47aea9d4a4e29e685894c8c75b997e507862c36da52f in / 
# Tue, 04 Oct 2022 23:45:22 GMT
CMD ["bash"]
# Tue, 04 Oct 2022 23:45:28 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5de3e49ea1c1676df95c2f1e0df1cedc8b8eedf184a3aa0b5afcf188e6043da2`  
		Last Modified: Tue, 04 Oct 2022 23:51:37 GMT  
		Size: 49.2 MB (49228863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5846890602b8cb6c6748989552b97a4cf57188ecc57d431d87c1dcfad50e55fc`  
		Last Modified: Tue, 04 Oct 2022 23:51:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5ac61557f86a69cae923e07bde5505b6f588e2ce8220fbf45be628b3b6c65479
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51208184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1c248c6deb5ad42b81fde402ec2c9ad5c6228ea920b42569c0730b6bb66f24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:23:13 GMT
ADD file:4308a4e31a597a68a869ed89293f56effa688d73fd2ef1f42b2167991e9191ea in / 
# Tue, 25 Oct 2022 02:23:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:23:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d1231a6244b56ad7b565bc454e1b6fb5c2945c1fa6d068d84483a508b2b20323`  
		Last Modified: Tue, 25 Oct 2022 02:29:41 GMT  
		Size: 51.2 MB (51207960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f379a5647c098ad3f5dc76518eba3bffefb41e46e8a4597b6280627158f5d`  
		Last Modified: Tue, 25 Oct 2022 02:29:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
