## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:df68b51d3bce7d91362f2a7faf59f51ea9a8aa51b13d69a82f2fcbd8059905b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:492309f2537f326af582de9301907b6155756f0045a8d04cf3aa7804d692a4fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50449323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e52e8b373b0af5e8e8a48f3c5c8c8fdaff7a31cc1aeb89d81ec29352339acd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:33 GMT
ADD file:12083e75f80fb6bd621143c2eb98ab9ce4dfe1b28b3cde8a86dbc6bd8e4bc7bd in / 
# Wed, 01 Mar 2023 04:10:33 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:10:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:555942b702dc4f48a84a3d5d879bbeabc861fb4e7f24cdbd5384c4aea9dfe591`  
		Last Modified: Wed, 01 Mar 2023 04:15:23 GMT  
		Size: 50.4 MB (50449095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306f771e7004b146336f5eaabe69cfc92544070412973d1c1532825f710dbf4`  
		Last Modified: Wed, 01 Mar 2023 04:15:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:34b7941b50ec36e2639b99b1de127c9a26ff694efc40e8e183c4a4e440b30699
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d52d5909bff9a48e8bfb27887fd4f0ca72a8930b61e64ba66dd6dfb99f84e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:58:21 GMT
ADD file:ccafb0d4746567d93ef1a3ac27400488eb9d41acb93e3a18f1e77377ff97c8f1 in / 
# Wed, 01 Mar 2023 01:58:21 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:58:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:548799b11fde653a3d163dd7bb5426257f268b7c2b7133518be0cd64df798a73`  
		Last Modified: Wed, 01 Mar 2023 02:04:13 GMT  
		Size: 45.9 MB (45916081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10367b73896194527344a35e5c5fa3746f93197523f34ef9b1c66a6faba22c22`  
		Last Modified: Wed, 01 Mar 2023 02:04:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:74a7bfdba6deface0fd6eb129e24ba466f44a16150c82af82befe9c6ec63f9d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49239950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a853a2cf140be3de76719487194d1dfe79994db1b69b7088539c62b9f9a8575`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:29 GMT
ADD file:3ca838a216948e310a97603cb0d9809d74545e5716bb4fc07adbe101331d351a in / 
# Thu, 23 Mar 2023 00:45:30 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:45:31 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bcffd7be664cb5f76625b6b2cfb4a0c025363fb1f228f6c32b05eb1acfe61188`  
		Last Modified: Thu, 23 Mar 2023 00:49:02 GMT  
		Size: 49.2 MB (49239727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a910a056ba2e8163f623e871d4ee317120d610d1350401255a547c54d8ec1466`  
		Last Modified: Thu, 23 Mar 2023 00:49:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:7dcdd9a8f4f1a42d478936d99b6b52617eba2c16bdc8ee00c90ec5dd09859783
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef85777f4ff00aed9ed34153960955501ba726af98e4aca36b7e29ce7855d37`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:50 GMT
ADD file:7a37d1452774d17cc1cdc4ef3b04834f1dc2ff2255df329ad99273bcff617b80 in / 
# Thu, 23 Mar 2023 00:39:50 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:39:53 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:35af01d500b72dc26ff46cb1e4d6300700fe5cad14db1a17127ff2faa2a3cdbe`  
		Last Modified: Thu, 23 Mar 2023 00:44:17 GMT  
		Size: 51.2 MB (51207092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302873df793766dc819b6a4e8512a7b38ff7a02e7789ab88e3577bd37e04d1d5`  
		Last Modified: Thu, 23 Mar 2023 00:44:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
