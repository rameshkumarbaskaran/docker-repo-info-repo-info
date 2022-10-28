## `nats:linux`

```console
$ docker pull nats@sha256:806d56dd55acbc6497c5cc9ff5916b36ba091212c7308b3a23a1098876e686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
