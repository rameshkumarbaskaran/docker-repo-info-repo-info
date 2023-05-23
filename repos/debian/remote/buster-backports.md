## `debian:buster-backports`

```console
$ docker pull debian@sha256:19b509ccfd2447d1df1aa8139a99665e0c69d9b7e85797b5e296af6df6da1e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:5eb1ab381fd8c1a43bca83c9daf058f59f516ed6fefc33f9e42277dc760949d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50448937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163dd8e303d1344f191c8af3bae282a85727cafd8ef9e9c421f255472000e001`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:20:29 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ec6b18fa13c21a10e989667b77659ccbee2bb520cb09b4aec068ce81e42017`  
		Last Modified: Tue, 23 May 2023 01:24:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:bd0ebd7a5310d9e5d3072cc401c719c70bbe4cbe89567044f2c65e42c37ff049
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b0823e6881b802706688b3574a4e50b0a02da8b3aaab751b514dbe633f6731`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:58:06 GMT
ADD file:a1ddba603e505863ad4f9d8c828c3d963fc27fef39de1fee725e8b790a1acfd0 in / 
# Tue, 23 May 2023 00:58:07 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:58:10 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ba419081a96034b68934ec792c30825d3deecc56745c9b286bb7637a393c2929`  
		Last Modified: Tue, 23 May 2023 01:02:04 GMT  
		Size: 45.9 MB (45916510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9347125defe597288a5bf9e2d2540e67cf28e18c2ebf818a4c8f2b5a5bd6a66`  
		Last Modified: Tue, 23 May 2023 01:02:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:586ea9c1db3db0541c971b1ed6e59ec75633b82529d93cae53834bb683f8c8cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49238514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8dd0a2d42a2a5850bff42400717823ab629154859555b4f8b82d65a8912818e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:21 GMT
ADD file:a5100e7ed3c2665c1b4dfbb32eb2b47b85783f2a6800e0ae9004db0ce021dfa5 in / 
# Tue, 23 May 2023 00:43:22 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:43:23 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5ea482247e9a0d1ae4ed218fb0828063b9cce53822e64fd4621f587ab85a7e6d`  
		Last Modified: Tue, 23 May 2023 00:46:24 GMT  
		Size: 49.2 MB (49238292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce59584923a0942b39a4e6d9ab50601535ce46dcfc15fa877b3340ec85d8bcc`  
		Last Modified: Tue, 23 May 2023 00:46:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:d490308e0a203e559b8620f9719b8dcc03c3153cc68c378fbc02017d2f807a5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51205902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244623dffe1ad3aa758a3b0665839681fd492c37db644695d2c8c90a31593829`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:39:45 GMT
ADD file:d82a514985e1c8796d6c5572290d84fdff0dc1c748d7d2e469d3066ac0344c5f in / 
# Tue, 23 May 2023 00:39:45 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:39:50 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5a48e9012f51ff679af95460521da76c7184da775e3adaa39fed65c912ce0a57`  
		Last Modified: Tue, 23 May 2023 00:44:49 GMT  
		Size: 51.2 MB (51205678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcecd95f3dad895deb16bb8f9e9067eb498fe96b72c0d4258e4173b388fc328`  
		Last Modified: Tue, 23 May 2023 00:45:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
